---
title: plenv-update作りました
date: 2013-11-11
tags:
- perl
---
[plenv-update](https://github.com/hfm/plenv-update/)というplenv用プラグインを作りました。
これは[rbenv-update](https://github.com/rkh/rbenv-update)の移植版で、plenvとそのプラグインを一度にアップデートするプラグインです。

## 使い方

ターミナルで `plenv update` と打つと使えます。

```
$ plenv update
updating plenv
 |  Already on 'master'
 |  From git://github.com/tokuhirom/plenv
 |  * branch            master     -> FETCH_HEAD
 |  Already up-to-date.

updating perl-build
 |  Already on 'master'
 |  From git://github.com/tokuhirom/Perl-Build
 |  * branch            master     -> FETCH_HEAD
 |  Already up-to-date.

updating plenv-update
 |  Already on 'master'
 |  From github.com:hfm/plenv-update
 |  * branch            master     -> FETCH_HEAD
 |  Already up-to-date.
```

rbenvもplenvも、それ自身と<LANG>-buildのアップデートをそれぞれするのが面倒だったので、これで少し楽できそうです。
