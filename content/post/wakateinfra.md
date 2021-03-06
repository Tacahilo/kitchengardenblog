---
date: 2015-02-23T13:00:00+09:00
title: '『若手インフラエンジニア現状確認会』を開催した #wakateinfra'
tags:
- infra
- event
---
若手インフラエンジニア現状確認会というイベントを開催しました。
全員発表型で、私([@hfm](https://twitter.com/hfm)), [@catatsuy](https://twitter.com/catatsuy), [@deeeet](https://twitter.com/deeeet), [@rrreeeyyy](https://twitter.com/rrreeeyyy), [@ryot_a_rai](https://twitter.com/ryot_a_rai), [@y_uuk1](https://twitter.com/y_uuk1)の6名（敬称略）が参加者です。

会場をご提供いただいた[@catatsuy](https://twitter.com/catatsuy)君とpixivの皆様方に感謝。

## 発表資料

「今までやってきたこと」「何故今の環境を選択したか」「選択の結果、何を得たか」「そして今、何をやりたいのか」という4つをテーマに発表しました。

<iframe src="//www.slideshare.net/slideshow/embed_code/key/En3tvmVxV5UAOR" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/hifumis/20150220-wakateinfraengineergenjohkakuninkai" title="若手インフラエンジニア現状確認会 @hfm #wakateinfra" target="_blank">若手インフラエンジニア現状確認会 @hfm #wakateinfra</a> </strong> from <strong><a href="//www.slideshare.net/hifumis" target="_blank">Takahiro Okumura</a></strong> </div>

ここから、資料補完や当日のやりとり、そもそもの開催の経緯等を補足したいと思います。

## 開催のキッカケ

開催といっても、Doorkeeperやconnpassで募集をかけたりせず、Twitterのリプライのみで実現した集まりです。
（ぼんやりとした企画をしたぐらいで、開催と呼べるほどなにかをやったわけではない）

[Mackerel Meetup #3 Tokyo](http://mackerelio.connpass.com/event/11047/)で[@y_uuk1](https://twitter.com/y_uuk1)君と喋ってたときに、「インフラエンジニアの数が少ない」「特に同世代（20代）はほんとに少ない」「会って話したいよね」みたいなやりとりをして、その帰り道にしたツイートをファボってくれた人達に「飲み会しよ」って言ったのが最初だったと思います。

#### 「飲もう」って言ってから現状確認会に発展するまでのやりとり（リプライ）の一部

飲み会から現状確認会へ進化してる様子です。

<blockquote class="twitter-tweet" lang="ja"><p lang="ja" dir="ltr"><a href="https://twitter.com/rrreeeyyy">@rrreeeyyy</a> <a href="https://twitter.com/deeeet">@deeeet</a> <a href="https://twitter.com/y_uuk1">@y_uuk1</a> 飲み会しよ <a href="http://t.co/zUehyYnP7v">pic.twitter.com/zUehyYnP7v</a></p>&mdash; okumura takahiro (@hfm) <a href="https://twitter.com/hfm/status/558265671209869312">2015, 1月 22</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" lang="ja"><p lang="ja" dir="ltr"><a href="https://twitter.com/rrreeeyyy">@rrreeeyyy</a> <a href="https://twitter.com/deeeet">@deeeet</a> <a href="https://twitter.com/hfm">@hfm</a> めっちゃよい！fyi <a href="https://twitter.com/catatsuy">@catatsuy</a></p>&mdash; yuuki (@y_uuk1) <a href="https://twitter.com/y_uuk1/status/558266295381020674">2015, 1月 22</a></blockquote>

<blockquote class="twitter-tweet" lang="ja"><p lang="ja" dir="ltr"><a href="https://twitter.com/deeeet">@deeeet</a> <a href="https://twitter.com/rrreeeyyy">@rrreeeyyy</a> <a href="https://twitter.com/hfm">@hfm</a> <a href="https://twitter.com/catatsuy">@catatsuy</a> 勉強会形式ということにすれば会社からお金でそうです</p>&mdash; yuuki (@y_uuk1) <a href="https://twitter.com/y_uuk1/status/558267791690563584">2015, 1月 22</a></blockquote>

<blockquote class="twitter-tweet" lang="ja"><p lang="ja" dir="ltr"><a href="https://twitter.com/hfm">@hfm</a> <a href="https://twitter.com/deeeet">@deeeet</a> <a href="https://twitter.com/y_uuk1">@y_uuk1</a> <a href="https://twitter.com/rrreeeyyy">@rrreeeyyy</a> ピクシブオフィスは他に予定がなければ使えますよ！セキュリティも他社よりゆるめなので色々楽です</p>&mdash; 麺類 (@catatsuy) <a href="https://twitter.com/catatsuy/status/558270101909028864">2015, 1月 22</a></blockquote>

<blockquote class="twitter-tweet" lang="ja"><p lang="ja" dir="ltr"><a href="https://twitter.com/hfm">@hfm</a> <a href="https://twitter.com/catatsuy">@catatsuy</a> <a href="https://twitter.com/deeeet">@deeeet</a> <a href="https://twitter.com/rrreeeyyy">@rrreeeyyy</a> <a href="https://twitter.com/y_uuk1">@y_uuk1</a> おお！ぜひ参加させていただきます！！</p>&mdash; Ryota Arai (@ryot_a_rai) <a href="https://twitter.com/ryot_a_rai/status/558289602096558081">2015, 1月 22</a></blockquote>

こんな感じで1〜2時間のふわっとした応酬の後、現状確認会の開催が決まったのでした。

## なぜ開催したのか

以下のツイートと発表資料がほぼ全てなんですが、20代のインフラエンジニアにとって「同世代」と呼べる人が本当に少ないと感じていて、率直に言えばライバルが欲しいってことかもしれません。

<blockquote class="twitter-tweet" lang="ja"><p lang="ja" dir="ltr"><a href="https://twitter.com/y_uuk1">@y_uuk1</a> <a href="https://twitter.com/deeeet">@deeeet</a> <a href="https://twitter.com/rrreeeyyy">@rrreeeyyy</a> <a href="https://twitter.com/catatsuy">@catatsuy</a> 冗談抜きで、お互い今何をやっていて、どこに興味があって、どういう方向性で頑張ってるか。めっちゃ興味あります</p>&mdash; okumura takahiro (@hfm) <a href="https://twitter.com/hfm/status/558268064941088771">2015, 1月 22</a></blockquote>

### 互いのバックグラウンドを知る

インフラエンジニアは何をやっているか見えづらい職業にも関わらず、何故その仕事を選んだのかにも興味がありました。
大学生のころの研究の話や会社に入ってから感じたこと・考えたことといった、お互いのバックグラウンドを話し合いたいという思いもありました。

そうした互いの状況を知ることで、「あいつはこんな凄いことをやってるし、俺も負けてられない！」というモチベーションをもらえるのではないか、という期待もありました（実際期待通りでした）。
特にそれが同世代であればこそ、同じような時間の流れを経験しているわけですから、共感出来るものも多かったように思います。

### 20代のインフラエンジニアが感じる危機感

また、X as a Serviceに標榜される分業化・クラウド化、「[インフラエンジニア(狭義)は死んだ](http://yapcasia.org/2014/talk/show/df196eac-fb65-11e3-b7e8-e4a96aeab6a4)」が示唆するこれからのインフラを考えると、「これからの10年、20年、あるいは定年までの40年」という生存戦略を考えなければいけないのでは、という危機感もありました。

まさしく、インフラエンジニアにとっての「現状確認の会」にしたいという思いが根本にありました。

## どんな雰囲気だったのか

### 結構自由

普通に各人用意したスライドをモニタに映しながらアレコレ喋るって感じなんですが、発表中でもお構いなしに、気になる箇所はバシバシ質問したり話し合ったり、時にはちょっぴり脱線したり（思い切り脱線したり）、自由で和気あいあいとした雰囲気でした。

### 各人の発表時間（めちゃくちゃ長い）

そんな自由闊達なやりとりもあって、発表時間がエグいことになり、19時半開始25時半終了という大長編となってしまいました。
色んな話をしたんですが、ほんとに話題が尽きなかった。

<blockquote class="twitter-tweet" lang="ja"><p lang="ja" dir="ltr"><a href="https://twitter.com/hashtag/wakateinfra?src=hash">#wakateinfra</a> <a href="https://twitter.com/ryot_a_rai">@ryot_a_rai</a> くんが「僕の発表一瞬で終わっちゃうと思います」って始めたのに、最終的に55分くらいの発表時間になってて最高だった。</p>&mdash; okumura takahiro (@hfm) <a href="https://twitter.com/hfm/status/569104204163198977">2015, 2月 21</a></blockquote>

持ち時間の長さ（みんなでワイワイ話しながらですが）だけで言えば、多分[@ryot_a_rai](https://twitter.com/ryot_a_rai)君が最大だった気がする。

## どんな話題が多かったか

### オペレーションの面倒さ

僕の感想では、とにかく「手作業からの解放」「自動化」「Operationを無くしたい」といったテーマが多かったように思います。

例えば、「dry-run -> runという作業の間には、『ちゃんと動いてそうか』という目grepがある。これは自動化できてない！」とか「DevOpsの次はNo Opsの時代が来るべき！」とか。
[@deeeet](https://twitter.com/deeeet)君の言葉を借りれば「筋肉運用」を無くそうという感じです。

### 自動化と複雑化

各人の考え方と工夫をもって、あらゆる作業を省力化・自動化しようと日々努力してると思いました。

そしてその為には「複雑なこと」は絶対に避けなければいけない、そのためにはどんな仕組み・設計が良いだろうか？
どのように啓蒙すべきか？
といった、「運用負担の軽減」も強く意識されているなあと思いました。

### たとえ明日お前が死んでも、インフラは価値を発揮し続けられるか

（見出しの煽り感）

インフラエンジニアにとって、（障害対応時などの）瞬発力も重要なスキルである一方、個人の経験値に依存しすぎることのリスク（バス係数・ドキュメントレス問題など）を皆さん感じているようでした。

インフラは勢いだけでガガッと作ればいいものではなくて、持続性を担保しなければ継続的な価値を発揮することができず、あっという間に恐ろしい技術的負債となって後に続く人たちにとっての重荷となりかねません。
皆さんの発表を聞くにつれ、「明日たとえ自分がいなくなっても、高い価値を発揮し続けられる柔軟で頑健なインフラ」を作らなければいけないなあと改めて強く意識させられました。

## 「若手」とは？

正直良くわかりません。

今回のイベントは入社して1〜3年ぐらいの人たちで開催しましたが、mizzyさんの仰る通り「若手かどうかはハートの問題」だと思います。

<blockquote class="twitter-tweet" lang="ja"><p lang="ja" dir="ltr">若手かどうかはハートの問題</p>&mdash; Gosuke Miyashita (@gosukenator) <a href="https://twitter.com/gosukenator/status/568719483772121088">2015, 2月 20</a></blockquote>

### 「若手ではない」「おっさん」とは？

個人的には、「そうは言ってもね...」みたいな言い訳が増えたらおっさんだな、と思います。
飽くなき挑戦心、諦めない粘り強さ、苦々しい現実を是としない強かさをもって、いつまでも若手の気持ちをもって頑張りたいです。

というわけで、次回開催があれば、定義を改めた「若手」のみんなで是非ワイワイしましょう！

<blockquote class="twitter-tweet" lang="ja"><p lang="ja" dir="ltr"><a href="https://twitter.com/hashtag/wakateinfra?src=hash">#wakateinfra</a> 呼ばれてないので若手ではない…のか…</p>&mdash; そらは (@sora_h) <a href="https://twitter.com/sora_h/status/568768130824081408">2015, 2月 20</a></blockquote>

<blockquote class="twitter-tweet" lang="ja"><p lang="ja" dir="ltr">行きたかったがチームの飲み会だったという。次回は参加したいっ(￣▽￣) <a href="https://twitter.com/hashtag/wakateinfra?src=hash">#wakateinfra</a></p>&mdash; Shohei Koyama (@sion_cojp) <a href="https://twitter.com/sion_cojp/status/569180167735676929">2015, 2月 21</a></blockquote>

<blockquote class="twitter-tweet" lang="ja"><p lang="ja" dir="ltr">老guyが必要になったら呼んでください… <a href="https://twitter.com/hashtag/wakateinfra?src=hash">#wakateinfra</a></p>&mdash; ひろせ３１ (@hirose31) <a href="https://twitter.com/hirose31/status/568800422904799232">2015, 2月 20</a></blockquote>

<blockquote class="twitter-tweet" lang="ja"><p lang="ja" dir="ltr"><a href="https://twitter.com/hashtag/wakateinfra?src=hash">#wakateinfra</a> 次回は京都で</p>&mdash; yuuki (@y_uuk1) <a href="https://twitter.com/y_uuk1/status/568814970424537089">2015, 2月 20</a></blockquote>

さて、ここから先は、発表資料の落ち穂拾いです。

## 「rpmビルド環境を自動化したい」のスライドについて

以下のブログ記事に刺激を受けて最近作った仕組みなんですが、結構悩みながら作ったので、その辺りの思考の過程も含めて1個の記事に起こしたいと思ってます。

- [Docker を用いた rpm / deb パッケージ作成の継続的インテグレーション - ゆううきブログ](http://yuuki.hatenablog.com/entry/docker-package-ci)

## なんでペパボ？

就活してた頃の意識ブレブレなダサい感じを話しました。

### 東京へのあこがれ

大学と大学院は名古屋だったんですが、その頃から東京のうっそうとしたエネルギーに焦がれるものがありました。
今も「東京」というブランドや無尽蔵かと思うほどのエネルギーの濁流は飽きないなあと。
（資料にも書いたとおり「体力の続くうちは...」って感じですが）

### 人事

就活当時、ペパボの人事の方の印象がとても強かったのを覚えています。
何人もの学生が面接を受けにゾロゾロやってくる中で、1回目の面接時のエピソードを覚えていただいていたり、「ものすごく人のことを見てくれる方だ」と感動したのを覚えています。

## IRCの様子

そういえば`#kernel`というチャンネルは思いのほか好評で、作って良かったなあと。

<blockquote class="twitter-tweet" lang="ja"><p lang="ja" dir="ltr">IRC の kernel channel めっちゃ欲しいしオープンチャンネルにして欲しい <a href="https://twitter.com/hashtag/wakateinfra?src=hash">#wakateinfra</a></p>&mdash; れい (Yoshikawa Ryota) (@rrreeeyyy) <a href="https://twitter.com/rrreeeyyy/status/568727490388037632">2015, 2月 20</a></blockquote>

### 嬉しいことはすぐ言うすぐ褒める

ペパボは複数のWebサービスを運営しており、サービスごとにエンジニアやデザイナ、サポートの方が所属しています。
そんなスタッフ同士がもっとも仕事でコミュニケーションを取る場所はIRCです。次点はおそらくGitHub Enterprise。

中でもエンジニアは特にIRCでのやりとりが多いのですが、スライドにもある通り、ほんの些細な喜びを伝えると「okkun++」と褒めてくれたりします。
自分一人で仕事をしてるんじゃない、と孤独を感じず仕事が出来るのも、ペパボの[大切にしてほしい3つのこと](http://pepabo.com/recruit/important/)が文化として成立しているからなんだろうな、と思います。

### iiirc.org

スライドに使ったIRCの様子は、ログが残ってなかったので http://iiirc.org/ からスクショを取ってきました。

- http://iiirc.org/snippets/444
- http://iiirc.org/snippets/486
- http://iiirc.org/snippets/491
- http://iiirc.org/snippets/501
- http://iiirc.org/snippets/505
- http://iiirc.org/snippets/515

## 今したいこと、カーネルの勉強

したいというか、目下取り組み中なのですが、カーネル分野に強い興味があって、Dockerに代表されるような新しい技術をドライブさせる魅力的な宝の山だと思っています。

ホスティングサービスをやってる背景もありますが、中でも[@hiboma](https://twitter.com/hiboma)さんの圧倒的な問題解決能力の高さにはお世話になりっぱなしで、「いつか自分も、同じように困っている人を助けたい」と強く思うようになりました。

また、[@matsumotory](https://twitter.com/matsumotory)さんが業務委託という形でペパボのお仕事をされているのですが、hibomaさんとmatsumotoryさんのお二人であれよあれよという間に問題を解決していく様子を見せられては、自分の進む道はここだと思わずにはいられなくなりました。

- [人間とウェブの未来 - 5月からペパボで仕事しています](http://blog.matsumoto-r.jp/?p=4205)

発表後に、[@rrreeeyyy](https://twitter.com/rrreeeyyy)君から「（発表にあったような）仕事をやった後に、カーネル分野に行こうとするのは珍しい」というニュアンスのコメントをいただいたのですが、インフラの「運用面」は減っていく一方で、インフラの「開発面」はまだまだ幅広く奥深い領域を持っており、ここに挑戦するのはやぶさかでないと考えています。

カーネルがインフラにとっての開発のように聞こえるかもしれませんが、「縁の下の力持ち」的な存在にかねてから憧れがあり、インフラエンジニアを軸足として、カーネル分野にも強くなれれば...といった感じです。  
（インフラという言葉を便利ワードにして使ってしまっているな、という感じはありますね...）

## 他の方の発表資料など

- [若手インフラエンジニア現状確認会で発表しました #wakateinfra - catatsuyとは](http://catatsuy.hateblo.jp/entry/2015/02/21/205303)
- [ある若手インフラエンジニアの現状確認 #wakateinfra // Speaker Deck](https://speakerdeck.com/tcnksm/aruruo-shou-inhuraenziniafalsexian-zhuang-que-ren-number-wakateinfra)
- [若手インフラエンジニア現状確認会 #wakateinfra に参加したまとめ - rrreeeyyy.com](http://rrreeeyyy.com/blog/2015/02/23/infra-younger/)

## おわりに

若者が使ってるハッシュタグを肉とか鍋画像でテロするのはおっさん。

<blockquote class="twitter-tweet" lang="ja"><p lang="ja" dir="ltr"><a href="https://twitter.com/hashtag/wakateinfra?src=hash">#wakateinfra</a> おっさんになって若者のハッシュタグ荒らすようになったら人生終わりだぞ</p>&mdash; yuuki (@y_uuk1) <a href="https://twitter.com/y_uuk1/status/568816217705721857">2015, 2月 20</a></blockquote>
