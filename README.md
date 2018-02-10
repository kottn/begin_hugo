# begin_hugo
:baby:はじめてのhugo

## やること
[GitHub Pages](https://pages.github.com/) + [Hugo](https://themes.gohugo.io/)
1. リポジトリ`https://github.com/<YourID>/<RepoName>`の中で自己紹介ページを作成し管理する
1. それを`https://<YourID>.github.io/<RepoName>`で見れるようにする（GitHub Pages の機能）
1. `html`が面倒だから`Markdown`で投稿できるようにする（Hugo の機能）

## 資料
[Hugo公式の資料](https://gohugo.io/hosting-and-deployment/hosting-on-github/)がわかるならそれがいちばん。

## 環境
Debian 9

## インストール
* https://github.com/gohugoio/hugo/releases にアクセス
* 最新の`*.deb`をダウンロード
* ダウンロード先に移動してインストール
```
cd ~/Downloads
sudo apt install *.deb
```
* 確認
```
hugo version
```

## リポジトリをつくる
* 今回作るリポジトリ`<RepoName>`は`mypage`とする（別になんでもいい）
* ディレクトリを`hugo`で作る

```
$ hugo new site mypage
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
