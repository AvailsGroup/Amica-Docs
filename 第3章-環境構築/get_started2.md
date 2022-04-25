# 第3章 - 環境構築

ここではAmicaをローカル環境で動かす方法を解説していきます。

これを見る前に[get_started](../第1章-はじめに/get_started.md)を参照してください。

- [第3章 - 環境構築](#第3章---環境構築)
  - [構築環境](#構築環境)
  - [ダウンロード](#ダウンロード)
  - [credentialsとmasterkeyを再生成](#credentialsとmasterkeyを再生成)
    - [編集ソフトの登録](#編集ソフトの登録)
    - [ファイルの削除](#ファイルの削除)
    - [ファイルの生成](#ファイルの生成)
    - [依存ライブラリのダウンロード](#依存ライブラリのダウンロード)
      - [Gem](#gem)
      - [yarn](#yarn)
    - [データーベースの生成](#データーベースの生成)
    - [起動](#起動)
  

## 構築環境

Windowsを想定して解説していきます。

## ダウンロード

【C:\Users\ユーザー名\Documents\workspace\Amica】を作業ディレクトリとします。

まずはエクスプローラーでworkspaceディレクトリを作成し、ファイルタブを押してPowershellで開くをクリックします。

```bash
git clone https://github.com/AvailsGroup/Amica.git
```

を実行します。

これでAmica自体のダウンロードは完了です。

```bash
cd Amica
```

で作業ディレクトリに移動しましょう。

## credentialsとmasterkeyを再生成

### 編集ソフトの登録

まずは環境変数にVCCodeを登録します。

システムの詳細設定 >> 環境変数 >> システム環境変数 >> 新規 をクリック

```text
変数名 EDITOR
変数値 code --wait
```

を登録後、適用してPCを再起動してください。

### ファイルの削除

config/credentials.yml.encを削除してください。

### ファイルの生成

```bash
rails credentials:edit
```

を実行し、VSCodeが開いたらcredentials.yml.templateの内容を貼り付けてください。

このファイルは必要になったらここにパスワードや見られてはいけない情報を格納しておくことで、Railsが自動で暗号化してくれます。

***同時に生成されるmasterkeyは他の人に漏らさないように注意してください。***

### 依存ライブラリのダウンロード 

#### Gem

```bash
bundle install --without production
```

このコマンドを実行することで本番環境以外のGemがインストールされます。

GemはRubyの拡張ライブラリです。

#### yarn

```bash
yarn install
```

このコマンドを実行することで依存関係にあるJavaScriptをダウンロードすることができます。

### データーベースの生成

```bash
rails db:create
rails db:migrate
```

createでデーターベースを作成し、migrateでテーブルの情報を追加してます。

生成されたDBは【database/development.sqlite3】です。

テーブルやカラムの情報が見たいときは【database/schema.rb】に全て書いてあります。

テーブルやカラムの情報のこれまでの変更が見たいときは【database/migrate】のマイグレーションファイルを参照しましょう。

### 起動

ここまでくればやっと起動することができます。

```bash
rails s
```

でrailsを実行できます。

http://localhost:3000

にアクセスしてみましょう。

ページが表示されたら完了です。お疲れさまでした。

質問やうまくいかない所があれば[Issue](https://github.com/AvailsGroup/Amica-Docs)にて対応しますのでお気軽に質問してくださいね。