# <img src="https://raw.githubusercontent.com/nim-lang/assets/master/Art/logo-crown.png" height="28px"/> Nim [![Build Status][badge-nim-travisci]][nim-travisci]

このリポジトリには Nimコンパイラ, Nimのstdlib, ツールおよびドキュメントが含まれています。
もっとNimについて知りたいときは, ドキュメントを含む最新リリースをダウンロードしてください。 [Nimのサイト][nim-site].

## コミュニティ(英語)
[![Join the IRC chat][badge-nim-irc]][nim-irc]
[![Join the Gitter chat][badge-nim-gitter]][nim-gitter]
[![Get help][badge-nim-forum-gethelp]][nim-forum]
[![View Nim posts on Stack Overflow][badge-nim-stackoverflow]][nim-stackoverflow-newest]
[![Follow @nim_lang on Twitter][badge-nim-twitter]][nim-twitter]

* [Nimのフォーラム][nim-forum] - Nimについて質問したり, 議論するには最高の場所です
* [#nim IRCチャンネル(Freenode)][nim-irc] - Nimについてリアルタイムで議論する場所です。
  また、ほとんどの開発決定はIRCで行われます。
* [Gitter][nim-gitter] - Nimについてリアルタイムで議論するための補助的な場です。
  GitterとIRCの間にはブリッジがあります。
* [Telegram][nim-telegram] - Nimについてリアルタイムで議論するための補助的な場です。
  これはNimの公式Telegramチャンネルです。
* [Stack Overflow][nim-stackoverflow] - プログラミング関連の一般的なQ&Aサイト。
  Nimについてのトピックがあります。
* [Github Wiki][nim-wiki] - その他のユーザーによるコンテンツ。

## コンパイル
コンパイラは現在、以下のプラットフォームと
アーキテクチャの組み合わせを公式にサポートしています:

  * Windows (Windows XP以降) - x86 と x86_64
  * Linux (すべてではないが、ほとんどをサポート) - x86, x86_64, ppc64 と armv6l
  * Mac OS X (10.04以降) - x86, x86_64 と ppc64

より多くのプラットフォームがサポートされていますが、定期的にテストされておらず、上記の
プラットフォームほど安定していない可能性があります。

次の手順通りに実行するとNimのコンパイルは非常に簡単です:

Nimコンパイラ自体がNimを利用して書かれているため、NimコンパイラのCで書かれた古いバージョンのソースが必要です。
それらはこちらから入手できます。[``nim-lang/csources``][csources-repo]リポジトリ


次に、ビルドに必要なものを用意します:

  * ``gcc`` 3.x/以降, ``clang``, ``Visual C++`` や ``Intel C++``などのコンパイラ。
    特に ``gcc`` 3.x 以降を使うことをお勧めします。
  * ``git`` もしくは ``wget`` ソースをリポジトリからダウンロードするために利用します。
  * Ubuntuで``gcc``を利用するときは``build-essential``パッケージを使います。
    (他のUbuntuディストリビューションでも同様です。) 

次に \*nix システム または Windows を利用している場合は、以下の手順でコンパイルする必要があります。
Nimをソースから ``gcc``, ``git`` と ``koch`` を利用してビルドする。
(``sh build.sh`` の代わりにx86 Windowsでは ``build.bat`` を、x86_64 Windowsでは ``build64.bat`` を利用してください。):

**注意: 以下のコマンドは開発版コンパイラのビルド手順です**
一般ユーザー向けの安定版はこちらです: https://nim-lang.org/install.html.

```
git clone https://github.com/nim-lang/Nim.git
cd Nim
git clone --depth 1 https://github.com/nim-lang/csources.git
cd csources
sh build.sh
cd ../
bin/nim c koch
./koch boot -d:release
./koch tools # Compile Nimble and other tools.
```

最後に、 インストールが完了したら (Windows, Mac  Linuxの場合は) 
パスに ``bin`` ディレクトリを通すことをお勧めします。

## Koch
``koch``はNimの様々な部分やドキュメント、Webサイトをを構築するために使用されるビルドツールです。
``koch``を使用してNimのテスト環境を構築することも可能です。

Nimの``bin``ディレクトリをパスに追加しているなら、
``./koch tests``でテストを実行できます。テストには時間がかかりますが、
カテゴリを指定してテストを行うこともできます。``./koch tests cat async``

``koch``について詳しくは[doc/koch.rst](doc/koch.rst) を参照してください。

## Nimble

``nimble`` はNimのパッケージマネジャーです。 詳しくは
[``nim-lang/nimble``][nimble-repo]を参照してください

## 貢献者

このプロジェクトは、貢献するすべての方々のおかげで成り立っています。 [Read on to find out how to contribute](#contributing).
<a href="https://github.com/nim-lang/Nim/graphs/contributors"><img src="https://opencollective.com/Nim/contributors.svg?width=890" /></a>

## 貢献する
[![Backers on Open Collective](https://opencollective.com/nim/backers/badge.svg)](#backers) [![Sponsors on Open Collective](https://opencollective.com/nim/sponsors/badge.svg)](#sponsors)
[![Setup a bounty via Bountysource][badge-nim-bountysource]][nim-bountysource]
[![Donate Bitcoins][badge-nim-bitcoin]][nim-bitcoin]
[![Open Source Helpers](https://www.codetriage.com/nim-lang/nim/badges/users.svg)](https://www.codetriage.com/nim-lang/nim)

私たちはどんな小さな修正でも歓迎します。
標準ライブラリのスペル修正から新たなモジュールの追加まですべてが歓迎され、評価されます。
貢献を開始する前に、以下のリポジトリ構造について理解しておいてください:

* ``bin/``, ``build/`` - これらのディレクトリはNimをビルドするまでは空です。
* ``compiler/`` - コンパイラのソースコード、また``compiler/nimfix``と``compiler/plugins``のコードも含まれます。
* ``nimsuggest`` - 以前は [``nim-lang/nimsuggest``][nimsuggest-repo] リポジトリにあった nimsuggest ツールです。 
* ``config/`` - コンパイラとドキュメントジェネレータの設定。
* ``doc/`` - ReStructuredText形式のドキュメントが格納されています。
* ``lib/`` - 標準ライブラリ、内容:
    * ``pure/`` - Nimだけで書かれたライブラリ。
    * ``impure/`` - Nimで書かれた他の言語に依存するライブラリ。
    * ``wrappers/`` - 依存するほかの言語によって書かれたライブラリ。
* ``tests/`` - コンパイラと標準ライブラリのためのテスト。
* ``tools/`` - ``niminst`` と ``nimweb`` を含む(主に``koch``経由で呼び出される)。
* ``web/`` - [Nim website][nim-site].
* ``koch.nim`` - Nimを自動生成するツール、Cソース、Webサイト、ドキュメントを生成するツール。

もしあなたがGitHubやgitを使ったプルリクエストに慣れていないなら:
[こちら][pull-request-instructions].

プルリクエストを送信する前にすべてのテストに合格することが理想的ですが、時間が足りない場合には
変更箇所に対応したテストを行うだけでも構いません。
Travis CIがプルリクエストを受け入れる前にテストします。
統合テストは ``tests/untestable``です。

貢献する方法をお探しの場合は[issue tracker][nim-issues]をご覧ください。
 [``Easy``][nim-issues-easy]ラベルの問題はたくさんあります。
これらはNimへの貢献の良い出発点となるはずです。

寄付をしてNimの開発の手助けをすることもできます。寄付は以下から行うことができます:

* [Open Collective](https://opencollective.com/nim)
* [Bountysource][nim-bountysource]
* [Bitcoin][nim-bitcoin]

ご質問がありましたら、[Nimフォーラム][nim-forum]やIRC[the \#nim channel][nim-irc]にお寄せください。


## 支持者

感謝します! [[Become a backer](https://opencollective.com/Nim#backer)]

<a href="https://opencollective.com/Nim#backers" target="_blank"><img src="https://opencollective.com/Nim/backers.svg?width=890"></a>


## スポンサー

スポンサーになることでこのプロジェクトをサポートしてください。 ロゴがあなたのウェブサイトへのリンクとともにここに表示されます。[[Become a sponsor](https://opencollective.com/Nim#sponsor)]

<a href="https://opencollective.com/Nim/sponsor/0/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/0/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/1/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/1/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/2/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/2/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/3/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/3/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/4/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/4/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/5/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/5/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/6/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/6/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/7/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/7/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/8/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/8/avatar.svg"></a>
<a href="https://opencollective.com/Nim/sponsor/9/website" target="_blank"><img src="https://opencollective.com/Nim/sponsor/9/avatar.svg"></a>

当ウェブサイトの[スポンサーページ](https://nim-lang.org/sponsors.html)には、様々な支払いサービスのスポンサー/支援者のリストも表示されます。

## ライセンス
コンパイラと標準ライブラリは、MITライセンスの下でライセンスされています。
すなわち、Nimで開発した独自のプログラムに互換性のあるライセンスを使用することができます。
Nimを使用して商用アプリケーションを開発することは明示的に許可されています。

ライセンスについての詳細は [copying.txt](copying.txt) をお読みください。

Copyright © 2006-2018 Andreas Rumpf, all rights reserved.

Translate by koki Kobayashi. 2018

[nim-site]: https://nim-lang.org
[nim-forum]: https://forum.nim-lang.org
[nim-issues]: https://github.com/nim-lang/Nim/issues
[nim-issues-easy]: https://github.com/nim-lang/Nim/labels/Easy
[nim-irc]: https://webchat.freenode.net/?channels=nim
[nim-travisci]: https://travis-ci.org/nim-lang/Nim
[nim-twitter]: https://twitter.com/nim_lang
[nim-stackoverflow]: https://stackoverflow.com/questions/tagged/nim
[nim-stackoverflow-newest]: https://stackoverflow.com/questions/tagged/nim?sort=newest&pageSize=15
[nim-gitter]: https://gitter.im/nim-lang/Nim
[nim-telegram]: https://t.me/nim_lang
[nim-bountysource]: https://www.bountysource.com/teams/nim
[nim-bitcoin]: https://blockchain.info/address/1BXfuKM2uvoD6mbx4g5xM3eQhLzkCK77tJ
[nimble-repo]: https://github.com/nim-lang/nimble
[nimsuggest-repo]: https://github.com/nim-lang/nimsuggest
[csources-repo]: https://github.com/nim-lang/csources
[badge-nim-travisci]: https://img.shields.io/travis/nim-lang/Nim/devel.svg?style=flat-square
[badge-nim-irc]: https://img.shields.io/badge/chat-on_irc-blue.svg?style=flat-square
[badge-nim-gitter]: https://img.shields.io/badge/chat-on_gitter-blue.svg?style=flat-square
[badge-nim-forum-gethelp]: https://img.shields.io/badge/Forum-get%20help-4eb899.svg?style=flat-square
[badge-nim-twitter]: https://img.shields.io/twitter/follow/nim_lang.svg?style=social
[badge-nim-stackoverflow]: https://img.shields.io/badge/stackoverflow-nim_tag-yellow.svg?style=flat-square
[badge-nim-bountysource]: https://img.shields.io/bountysource/team/nim/activity.svg?style=flat-square
[badge-nim-bitcoin]: https://img.shields.io/badge/bitcoin-1BXfuKM2uvoD6mbx4g5xM3eQhLzkCK77tJ-D69134.svg?style=flat-square
[pull-request-instructions]: https://help.github.com/articles/using-pull-requests/
[nim-wiki]: https://github.com/nim-lang/Nim/wiki
