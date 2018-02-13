# begin_hugo
:baby:はじめてのhugo

## やること
[GitHub Pages](https://pages.github.com/) + [Hugo](https://themes.gohugo.io/) で自己紹介ページを作る
1. リポジトリ`https://github.com/<アカウント名>/<リポジトリ名>`の中でページを作成・管理する
1. それを`https://<アカウント名>.github.io/<リポジトリ名>`で見れるようにする（GitHub Pages の機能）
1. そんなに凝ったものじゃなくていいから`HTML`じゃなくて`Markdown`で全部やる（Hugo の機能）

## 資料
* [Hugo公式の資料](https://gohugo.io/hosting-and-deployment/hosting-on-github/)がわかるならそれで十分です。
* [完成イメージ](https://kottn.github.io/mypage)

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

## リポジトリをつくる
* 今回作るリポジトリ`<リポジトリ名>`は`mypage`とする（別になんでもいい）
* そのディレクトリは`hugo`コマンドでテンプレート付きで作る
```
$ hugo new site mypage    #テンプレート生成
$ tree -F mypage
mypage/
|-- archetypes/
|   `-- default.md
|-- config.toml
|-- content/
|-- data/
|-- layouts/
|-- static/
`-- themes/
6 directories, 2 files
```

## 好みのテーマを選ぶ

https://themes.gohugo.io


