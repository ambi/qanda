# MkDocs

[MkDocs](https://www.mkdocs.org/) は、静的サイトジェネレータである。Ruby 製の [Jekyll](https://jekyllrb.com/) や Go 製の [Hugo](https://gohugo.io/) が有名だが、Python 製の MkDocs は機能的にはかなりシンプルな部類に入る。ただ、わたしが期待している機能がちょうどいい感じにあった。

- Markdown で書くと HTML に変換されて表示される。
- 静的にサイトを生成する。（ので、GitHub Pages などで簡単にデプロイできる）
- 様々なテーマがあって、デザインを変えられる。
- ローカルでライブリロードのサーバを立ち上げて、編集中のサイトをプレビューできる。

ここまでは普通の静的サイトジェネレータの機能。

- ナビゲーションには、Markdown ファイル（ページ）を新規に作ると、自動でページヘのリンクが追加される。これは [`nav`](https://www.mkdocs.org/user-guide/configuration/#nav) という設定項目のデフォルト設定にすぎないが、そういうことをちょうどやりたかった。
  - ただ、これはアルファベット順だが、作成日時順や更新日時順にしたいといった話になるとすぐに無理になるから、やはり機能はいまいち足りていない。Hugo では[順序のカスタマイズ](https://gohugo.io/templates/lists/)はかなりできる。
- サイトの検索フォームが付いている。ほとんどのテーマでは日本語検索には未対応だが、[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) テーマは日本語も対応している。
  - [Hugo でも検索を実現する](https://gohugo.io/tools/search/)こともできるが、やり方は簡単でない。自動でやってくれる MkDocs は楽。
- GitHub Pages へのデプロイが、`mkdocs gh-deploy` の１コマンドでできる。

さくっと作るには MkDocs は便利だった。ただ、ちゃんとカスタマイズすることを考えると結局、Hugo を MkDocs 的に使えるように整備したほうがよさそう。ナビゲーションはテーマのカスタマイズでできるし、GitHub Pages へのデプロイもシェルスクリプトを用意すれば１コマンドにできるが、検索だけはちょっと面倒。