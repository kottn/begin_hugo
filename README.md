# begin_hugo
:beginner: はじめてのhugo

## hugo?
* 記事用のテンプレートファイルを元にHTMLファイルを生成してくれるツール。
* 楽にマイページが作れる・更新できる。

## やること
[GitHub Pages](https://pages.github.com/) + [Hugo](https://themes.gohugo.io/) で自己紹介ページを作る
1. リポジトリ`https://github.com/<アカウント名>/<リポジトリ名>`でコンテンツを管理する
1. それを`https://<アカウント名>.github.io/<リポジトリ名>`にてHP的に表示する（GitHub Pages の機能）
1. シンプルなサイトでいいから`HTML`じゃなくて`Markdown`で楽に管理する（Hugo の機能）

## 参考資料
* [Hugo公式](https://gohugo.io/hosting-and-deployment/hosting-on-github/)
* [日本語資料](https://qiita.com/eichann/items/4fe61b8b9bbafcfbe847)
<!-- * [完成イメージ](https://kottn.github.io/mypage) -->

## 環境
Debian 9 / Ubuntu 16.04

## hugo のインストール
* https://github.com/gohugoio/hugo/releases にアクセス
* 最新の`hugo_*.deb`をダウンロード
* ダウンロード先に移動してインストール
```
$ cd ~/Downloads
$ sudo apt install hugo_*.deb
```
* ちなみに Go 言語製だが Go はいらない

* コマンド確認
```
$ hugo version
```

## サイトをつくる
### サイト生成
* 今回は`<リポジトリ名>`=`mypage`とする（※別になんでもいい）
```
$ hugo new site mypage
```
* 生成物
```
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

### テーマを選ぶ
* [公式テーマ](https://themes.gohugo.io)から好きなのを選ぶ。
* ここからは試しに[Temple](https://themes.gohugo.io/temple/)というテーマでやってみる。

### 初期設定
1. テーマを`clone`する
    ```
    $ cd themes && git clone https://github.com/aos/temple.git
    ```
1. テーマやサイト名などを`config.toml`に書く  
    ```
    $ cat config.toml
    baseURL = "https://kottn.github.io/mypage"
    languageCode = "ja"
    title = "kottn's posts"
    theme = "temple"

    [permalinks]
        posts = "/:year/:month/:slug/"

    [params]
      # Enables syntax highlighting
      highlight = true 

      # Supports highlighting for languages not included in the original pack
      # See https://highlightjs.org/download/ for what's included in original pack
      # For reference to all languages, see:
      # https://github.com/isagalaev/highlight.js/tree/master/src/languages
      hjslangs = ["go", "vim"]

      # Enables the topmenu, which pulls from categories
      topmenu = "categories"

    # Builds a list page for each category given
    [taxonomies]
      tag = "tags"
      category = "categories"

    [author]
      name = "kottn"
      github = "kottn"
      twitter = "kottn_jp"
    ```

### 早速書いてみる
1. 記事のフォーマットを作成、編集。
    ```
    $ hugo new post/hello-world.md  # => /mypage/content/post/hello-world.md が生成
    $ vi content/post/hello-world.md
    ```
    ```
    ---
    title: "Hello World"             # 自動
    date: 2018-03-13T19:14:03+09:00  # 自動
    draft: true                      # 自動
    ---

    ## Hi !
    ### こんにちは！これが私の hugo 初投稿です。      # 追記
    #### 皆さん、よろしくお願いいたします！           # 追記

    * 箇条書きも  # 追記
    * できるよ    # 追記
    ```

1. ローカルで見てみる
    1. hugo server (確認用のローカルサーバ）を立ち上げる
    ```
    $ hugo server -D    # mypage/ 下で実行
    ```
    1. ブラウザのURL欄：`localhost:1313/mypage/`としてEnter
    1. みれる

    

