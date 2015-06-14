---
layout: post
date: 2015-05-28 23:32:23 +0900
title:  ― 「ウェブオペレーション」を読んだ
tags:
- book
---

#### 目次

- 1章  ウェブオペレーション：キャリア
  - 1.1  なぜウェブオペレーションが難しいのか？
  - 1.2  アプレンティスからマスターへ
  - 1.3  結論
- 2章  Picnikにおけるクラウドコンピューティングの利用とその教訓
  - 2.1  クラウドが適しているところ（とその理由！）
  - 2.2  クラウドが適していないところ（Picnikの場合）
  - 2.3  結論
- 3章  インフラとアプリケーションのメトリクス
  - 3.1  時間分解能と保存項目
  - 3.2  メトリクスの収集・保存における地域性
  - 3.3  メトリクスのレイヤ
  - 3.4  異常検出とアラート
  - 3.5  ログもメトリクス
  - 3.6  変更管理とインシデント時間の関係
  - 3.7  アラートでメトリクスを活用する
  - 3.8  メトリクスを使った負荷フィードバックメカニズムの調整
  - 3.9  メトリクス収集システムの例（Ganglia）
  - 3.10  結論
- 4章  継続的デプロイ
  - 4.1  小さなバッチはフィードバックが早い
  - 4.2  小さなバッチは問題を局所化する
  - 4.3  小さなバッチはリスクを減らす
  - 4.4  小さなバッチはオーバーヘッドを減らす
  - 4.5  品質管理者の嘆き
  - 4.6  さあ始めよう
  - 4.7  継続的デプロイはミッションクリティカルなアプリケーションに
  - 4.8  結論
- 5章  コードとしてのインフラ
  - 5.1  サービス指向アーキテクチャ
  - 5.2  結論
- 6章  監視
  - 6.1  物語「旅の始まり」
  - 6.2  手順1：監視対象を理解する
  - 6.3  手順2：通常の動作を理解する
  - 6.4  手順3：準備して学ぶ
  - 6.5  結論
- 7章  いかにして複雑なシステムは失敗するか
  - 7.1  いかにして複雑なシステムは失敗するか
  - 7.2  ウェブオペレーションに関すること
  - 7.3  補足資料
- 8章  コミュニティ管理とウェブオペレーション
- 9章  予期しないトラフィック急増への対応
  - 9.1  事の始まり
  - 9.2  アラーム三昧
  - 9.3  火消し
  - 9.4  週末を生き延びる
  - 9.5  将来への備え
  - 9.6  CDNの救援
  - 9.7  プロキシサーバ
  - 9.8  スタンピードを捕まえる
  - 9.9  コードの整理
  - 9.10  確認
  - 9.11  本物のテスト
  - 9.12  教訓
  - 9.13  日々改善
- 10章  開発と運用の協力と連携
  - 10.1  デプロイ
  - 10.2  共有のオープンなインフラ
  - 10.3  信頼
  - 10.4  オンコール開発者
  - 10.5  非難を避ける
  - 10.6  結論
- 11章  訪問者の気持ち：ユーザ対面メトリクス
  - 11.1  なぜユーザ対面メトリクスを収集するのか？
  - 11.2  なぜサイトが遅くなるのか？
  - 11.3  遅延の計測
  - 11.4  SLAの構築
  - 11.5  訪問者の成果：解析
  - 11.6  マーケティングが気にするその他のメトリクス
  - 11.7  ユーザエクスペリエンスのウェブオペレーションへの影響
  - 11.8  ウェブ監視の未来
  - 11.9  結論
- 12章  ウェブにおけるリレーショナルデータベースの戦略と戦術
  - 12.1  ウェブデータベースの要件
  - 12.2  典型的なウェブデータベースの成長
  - 12.3  クラスタあこがれ
  - 12.4  データベース戦略
  - 12.5  データベース戦術
  - 12.6  結論
- 13章  障害を活用する：ふりかえりの技芸と科学
  - 13.1  最悪のふりかえり
  - 13.2  ふりかえりとは
  - 13.3  ふりかえりの時期
  - 13.4  ふりかえりの参加者
  - 13.5  ふりかえりの実施
  - 13.6  ふりかえりのあとで
  - 13.7  結論
- 14章  ストレージ
  - 14.1  データ資産の棚卸し
  - 14.2  データ保護
  - 14.3  キャパシティ計画立案
  - 14.4  ストレージのサイジング
  - 14.5  オペレーション
  - 14.6  結論
- 15章  非リレーショナルデータベース
  - 15.1  NoSQLデータベースの概要
  - 15.2  NoSQLデータベースの詳細
  - 15.3  結論
- 16章  アジャイルインフラストラクチャ
  - 16.1  アジャイルインフラストラクチャ
  - 16.2  で、何が問題なの？
  - 16.3  利益共同体とプラクティスのコミュニティ
  - 16.4  トレーディングゾーンと謝罪
  - 16.5  結論
- 17章  夜中に聞こえる奇妙な物音（と、ぐっすり眠る方法）
  - 17.1  定義
  - 17.2  9はいくつ？
  - 17.3  「影響継続」対「事故継続」
  - 17.4  データセンタの足跡
  - 17.5  劣化障害
  - 17.6  誰も信じない
  - 17.7  フェイルオーバーのテスト
  - 17.8  監視とパターンの歴史
  - 17.9  ぐっすり眠る
- 18章  日本の料理のインフラ
  - 18.1  クックパッドを動かすサーバ群
  - 18.2  厳格なレスポンスタイムとその監視
  - 18.3  キャパシティ（リソース）の管理
  - 18.4  ソースコードだけでない履歴管理
  - 18.5  情報共有の取り組み
  - 18.6  必要ならばアプリケーションも書く
  - 18.7  抱える課題
  - 18.8  終わりに

<div class="booklog_html"><table><tr><td class="booklog_html_image"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4873114934/hifumiass-22/ref=nosim/" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51-ThZ6FRfL._SL160_.jpg" width="117" height="150" style="border:0;border-radius:0;" /></a></td><td class="booklog_html_info" style="padding-left:20px;"><div class="booklog_html_title" style="margin-bottom:10px;font-size:14px;font-weight:bold;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4873114934/hifumiass-22/ref=nosim/" target="_blank">ウェブオペレーション ―サイト運用管理の実践テクニック (THEORY/IN/PRACTICE)</a></div><div style="margin-bottom:10px;"><div class="booklog_html_author" style="margin-bottom:15px;font-size:12px;;line-height:1.2em">著者 : </div><div class="booklog_html_manufacturer" style="margin-bottom:5px;font-size:12px;;line-height:1.2em">オライリージャパン</div><div class="booklog_html_release" style="font-size:12px;;line-height:1.2em">発売日 : 2011-05-14</div></div><div class="booklog_html_link_amazon"><a href="http://booklog.jp/item/1/4873114934" style="font-size:12px;" target="_blank">ブクログでレビューを見る»</a></div></td></tr></table></div>