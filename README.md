# スライドの作り方

参考サイト

- [reveal.js + Markdown + GitHub Pagesでスライド公開](https://qiita.com/y_shoji/items/8df93817a8b8c2444f7b)
- [reveal.js + markdownでスライドを作る時は reveal-ck が便利だった](https://sue445.hatenablog.com/entry/2015/10/03/201241)

使用モジュール

- [hakimel/reveal.js](https://github.com/hakimel/reveal.js/)

### スライド作成

```
reveal-ck generate
```

### サーバ立ち上げ

```
reveal-ck serve
```

デフォルトで localhost:10000 に立つので、ブラウザで開く。  
編集し保存するたびに自動リロードする。

### gh-pagesブランチ

- masterブランチの .gitignore に slides/ を登録
- git checkout --orphan gh-pages で親commitがないgh-pagesブランチを作成
- git commit --allow-empty で空コミット作ってpush
- git clone [git url] --branch gh-pages --single-branch ./[任意のディレクトリ名] で[任意のディレクトリ名]配下にgh-pagesのみをclone
- cd [任意のディレクトリ名]
- reveal-ck generate でslides/ ファイルを作成
- commit & push したらそれがgh-pagesに反映される

### gh-pagesでの確認

https://doragon.github.io/slide-revealjs/slides/#/
