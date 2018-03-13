# begin_hugo
:beginner: はじめてのhugo

## hugo?
* 記事用のテンプレートファイルを元にHTMLファイルを生成してくれるツール。
* 楽にマイページが作れる・更新できる。

## やること
[GitHub Pages](https://pages.github.com/) + [Hugo](https://themes.gohugo.io/) で自己紹介ページを作る
1. リポジトリ`https://github.com/<アカウント名>/<リポジトリ名>`でページを管理する
1. 他の人はそれを`https://<アカウント名>.github.io/<リポジトリ名>`で見れる（GitHub Pages の機能）
1. シンプルなサイトでいいから`HTML`じゃなくて`Markdown`で管理する（Hugo の機能）

## 資料
* [Hugo公式の資料](https://gohugo.io/hosting-and-deployment/hosting-on-github/)がわかるならそれで十分です。
* [貴重な日本語資料](https://qiita.com/eichann/items/4fe61b8b9bbafcfbe847)
<!-- * [完成イメージ](https://kottn.github.io/mypage) -->

## 環境
Debian 9

## インストール
* https://github.com/gohugoio/hugo/releases にアクセス
* 最新の`*.deb`をダウンロード
* ダウンロード先に移動してインストール
```
$ cd ~/Downloads
$ sudo apt install *.deb
```

* 確認
```
$ hugo version
```

## サイトをつくる
### サイト生成
* 今回作るリポジトリ`<リポジトリ名>`：`mypage` ※別になんでもいい
* `hugo`コマンドで`mypage`というテンプレートディレクトリをつくる
```
$ hugo new site mypage    #テンプレート生成
$ tree mypage
mypage/
|-- archetypes/
|   `-- default.md
|-- config.toml
|-- content/
|-- data/
|-- layouts/
|-- static/
`-- themes/
```

### 記事生成

### テーマを選ぶ

* [ここ](https://themes.gohugo.io)から。

## 
