# 第1章 - はじめに

Amicaを使用するにあたって、開発環境や必要なソフトウェアを紹介していきます。 

- [第1章 - はじめに](#第1章---はじめに)
- [はじめに](#はじめに)
- [インストール](#インストール)
  - [開発環境](#開発環境)
  - [必須ソフトウェア](#必須ソフトウェア)
  - [開発環境構築](#開発環境構築)
    - [Ruby](#ruby)
    - [node](#node)
    - [yarn](#yarn)
  - [推奨ソフトウェア](#推奨ソフトウェア)
    - [git](#git)
    - [RubyMine](#rubymine)
    - [VisualStudioCode](#visualstudiocode)
  - [上級者向け](#上級者向け)
    - [Docker](#docker)


# はじめに

私たちは3ヶ月という限られた時間で設計、知らない言語での開発をおこないました。

Ruby on Railsを習得するコツはProgate等の学習サイトを使うことではなく、実際に制作してみてわからないことは知り合いのプロフェッショナルの方に聞いていました。

わからないな、むずかしいな、どうやって実装すればいいのかなと悩んだときはまずはよくGoogleで調べてみてください。

それでもわからなければぜひ私達を頼ってください。

このリポジトリのIssueやAmicaのチャット、Twitterなどまでいつでも聞きに来てくださいね。


# インストール

## 開発環境 

Windowsを想定して解説していきます。

## 必須ソフトウェア

Ruby 3.0.1 

node.js(yarn)

## 開発環境構築

### Ruby

まずはRubyInstallerからRuby3.0.1をダウンロードしていきます。

https://rubyinstaller.org/downloads/archives/

こちらからRuby+Devkit InstallersもしくはRubyInstallersの3.0.1をダウンロード、インストールしてください。

![image0](https://github.com/AvailsGroup/Amica-Docs/blob/master/images/image0.png "image0")

詳しいインストール方法は各自調べてみてください。

「Ruby Intaller Windows」等で検索するとすぐにヒットすると思います。

### node

Node.jsの公式サイトからインストーラをダウンロード、インストールします。

https://nodejs.org/ja/

安定している推奨版で構いません。

### yarn

yarnの公式サイトからインストーラをダウンロード、インストールします。

https://classic.yarnpkg.com/lang/en/docs/install/#windows-stable

![image1](https://github.com/AvailsGroup/Amica-Docs/blob/master/images/image1.png "image1")

わかりにくいですが「Alternatives」の「Click to expand / collapse」をクリックするとインストーラをダウンロードできます。

## 推奨ソフトウェア 

### git 

https://git-scm.com/

Amicaのクローン(ダウンロード)や本番サーバーにデプロイ(アップロード)する際に使います。

なくても大丈夫ですが、あったほうが安定した開発ができます。


### RubyMine

https://www.jetbrains.com/ja-jp/ruby/

統合開発環境です。

Rubyに特化していて圧倒的に使いやすいIDEです。

有料ソフトウェアですが、学生は無料です。絶対に使った方がいい

### VisualStudioCode

https://azure.microsoft.com/ja-jp/products/visual-studio-code/

こちらもコードエディターです。

RubyMineを使わない方はこっちの方がいいと思います。

RubyMineを使用している方も暗号化ファイルを編集するのに使うのでダウンロードしておいたほうがいいかもしれません。

## 上級者向け 

### Docker 

https://www.docker.com/

本アプリケーションの開発にはDockerを用いることもできます。

構築方法は[こちら](docker.md)を御覧ください。