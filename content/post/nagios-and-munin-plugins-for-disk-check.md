---
title: 最近書いた、SMART値からディスクセクタを監視するNagiosとMuninのプラグインの紹介
date: 2014-04-24
tags: 
- nagios
- munin
---
仕事でSMART値を利用したnagios, muninのプラグインを作ってました。

 * https://github.com/hfm/nagios-plugins
 * https://github.com/hfm/munin-plugins

## 必要なもの: smartmontools (smartctl)

`-d auto`を使えるバージョンが良いです。
Changelogによると、ver 5.40 (2010/10/16) あたりから使えるようです。

> http://sourceforge.net/apps/trac/smartmontools/browser/trunk/smartmontools/ChangeLog-5.0-6.0#L1343

CentOS 5以上であればyumから入ったので、RHEL系であれば`yum update smartmontools`で良さそうです。
バージョンアップしていくと`-d auto`で検出可能なデバイスタイプが増えていくので、新しいのがオススメです。

## Reallocated\_Sector\_Ct (SMART ID:5)

1つ目はReallocated\_Sector\_Ctを監視するプラグインです。

 * https://github.com/hfm/nagios-plugins/blob/master/check_bad_sector
 * https://github.com/hfm/munin-plugins/blob/master/bad_sector

```
ID# ATTRIBUTE_NAME          FLAG     VALUE WORST THRESH TYPE      UPDATED  WHEN_FAILED RAW_VALUE
  5 Reallocated_Sector_Ct   0x0013   100   100   050    Pre-fail  Always       -       0
```

Reallocated\_Sector\_Ctは不良セクタを予備セクタへ置換した数を示します。

ハードドライブはread, write verification等でエラーを発見すると、エラー対象のセクタを予約領域へデータ転送して置換（再配置、またはremap）を施行します。

そこまでクリティカルな現象では無いものの、RAW\_VALUEが溜まっていくに連れてread/writeの性能が悪くなるらしく、ある程度値が蓄積してきたらディスク交換をしたほうが良いでしょう。

### サンプル

カウント０の状態。現時点では不良セクタが見つかっておらず、概ね健康そう。

![](/images/2014/04/24/reallocated_sector_ct_safe.png)

一部デバイスにおいてremapされたグラフ。
この数字が増加につれて、ディスクの性能劣化につながっていく（ただし値と性能劣化の関係性は製品によると思うので、一概に50出たらアウト、とか言い切るのは難しいです）。

見ていて気持ちのいい数字じゃないですね。

![](/images/2014/04/24/reallocated_sector_ct_unhealthy.png)

## Current\_Pending\_Sector (SMART ID:197)

2つ目はCurrent\_Pending\_Sectorを監視するプラグインです。

 * https://github.com/hfm/nagios-plugins/blob/master/check_pending_sector
 * https://github.com/hfm/munin-plugins/blob/master/pending_sector

```
ID# ATTRIBUTE_NAME          FLAG     VALUE WORST THRESH TYPE      UPDATED  WHEN_FAILED RAW_VALUE
197 Current_Pending_Sector  0x0012   100   100   000    Old_age   Always       -       0
```

Current\_Pending\_Sectorは不良セクタの数を示します。
代替処理 (remapped) 待ちや、読み込みが出来ず回復不能なセクタなどがカウントされます。

fsckの実行やblockのゼロクリア(`dd if=/dev/zero of=<dev> seek=<block>`)で回復する（代替処理される）場合があり、回復すると値は減少します。
先ほどのReallocatedに比べるとクリティカルな現象で、ドライブ不調につきリプレイスを推奨されてます。

### サンプル

再配置されていない不良セクタが見つかっていないグラフ。
sdaとsdbはデバイスがSMART ID:197をサポートしておらず、値が取れませんでした。

1のところに先が引かれてるけど、warning/criticalのラインなのであしからず。

![](/images/2014/04/24/current_pending_sector_safe.png)

80近い不良セクタがあるヒヤヒヤもののデバイスがいるグラフ。
Reallocated\_Sector\_Ctと違って、不良セクタが不良セクタとして残ってしまっているため、何が起こるかわからないので早く置換した方がいい状態。

![](/images/2014/04/24/current_pending_sector_unsafe.png)

さっき見つけた悲鳴を上げたくなるグラフ。跳ね上がるな、跳ね上がるな。

![](/images/2014/04/24/current_pending_sector_jumpup.png)

## 使い方

どちらもbashで書いたので、プラグインディレクトリに置いて使っていただければ。

muninプラグインの作り方や導入に関してはこちらのブログを参考にさせていただきました。

> [Munin プロセスごとのスワップサイズを監視するMuninプラグインを作ってみた | ぱち ブログ](http://www.maepachi.com/blog/entry/142)

`/etc/munin/plugin-conf.d`に以下のようなファイルを用意して、上記プラグインをプラグインディレクトリに設置すると動くようになるみたいです。

```
[bad_sector]
user root
```

## なんでこのプラグインを作ったか

ディスクの経年劣化や初期不良により、満足にデータをホスト出来ないディスクを検知出来れば、計画的にディスクを交換し、サービスの安定した運用に貢献出来そうだと思って作りました。

## 検討中なこと

warning/criticalの閾値がこれでいいのか、という問題があります。

Current\_Pending\_Sectorは一個でも出ると、不良セクタが不良セクタのまま残っているのでcritical出すようにしてるんですが、Reallocated\_Sector\_Ctの閾値は運用しつつ様子を見てる感じです(10でwarning、20でcriticalにしてます)。

### 参考

だいたい以下と英語のWikipediaを読んで勉強しました。
英語版WikipediaのSMART値は説明的で良いです。

 * [S.M.A.R.T. Attribute: Reallocated Sectors Count | Knowledge Base](https://kb.acronis.com/content/9105)
 * [S.M.A.R.T. Attribute: Current Pending Sector Count | Knowledge Base](https://kb.acronis.com/content/9133)
