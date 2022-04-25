# 第2章 - 構成

ここではAmicaの全ファイル構成を載せていきます。

今後の開発の参考にしてください

- [第2章 - 構成](#第2章---構成)
- [ルートファイル構成](#ルートファイル構成)
- [Appファイル構成](#appファイル構成)
- [他によく使うファイル](#他によく使うファイル)

# ルートファイル構成 
```
Amica
├ app ...Railsのメインファイル関連が格納されています。
├ bin ...Railsの実行ファイル関連が格納されています。
├ config ...設定ファイルが格納されています。
├ db ...データーベース関連ファイルが格納されています。
├ lib ...多分未使用ディレクトリです。
├ log ...ログ関連が格納されています。
├ node_modules ...nodeでインストールしたファイルが格納されています。
├ public ...公開されるファイルが格納されています。
├ spec ...テスティング関連のファイルが格納されています。
├ storage ...未使用ディレクトリです。
├ tmp ...一時ファイルが格納されています。
├ vendor ...未使用ディレクトリです。
├ .browserslistrc
├ .env ...環境設定を記述するファイルです
├ .generators
├ .gitattributes
├ .gitignore ...gitにcommitしないディレクトリ、ファイルを指定するファイルです。
├ .rspec
├ .ruby-version
├ babel.config.js
├ config.ru
├ docker-compose.yml ...Dockerの関連ファイルです。
├ Dockerfile ...Dockerの関連ファイルです。
├ entrypoint.sh
├ Gemfile ...Gemのライブラリ管理ファイルです。
├ Gemfile.lock ...Gem関連のファイルです。
├ LICENSE ...ライセンスです。
├ package.json ...npm/yarnのライブラリ管理ファイルです。
├ postcss.config.js
├ Procfile
├ Rakefile
├ README.md ...説明書です。
└ yarn.lock ...yarn関連のファイルです。
```

# Appファイル構成

```
app
├ admin ...管理ページ関連のファイルが格納されています。
├ assets ...アセットパイプラインを使用する関連のファイルが格納されています。
├ channels ...websocket関連のファイルが格納されています。
├ controllers ...コントローラーのファイルが格納されています。
├ decorators ...デコレーターのファイルが格納されています。
├ helpers ...ヘルパーのファイルが格納されています。
├ javascript ...javascriptのファイルが格納されています。
├ jobs ...ジョブのファイルが格納されています。
├ mailers ...メーラーのファイルが格納されています。
├ models ...モデルのファイルが格納されています。
├ uploaders ...CarrierWave関連のファイルが格納されています。
└ views ...ビュー関連のファイルが格納されています。
```

# 他によく使うファイル

```
config\routes.rb ...ルーティングを管理するファイルです
db\migrate\* ...マイグレーションファイルです。
db\schema.rb ...データーベースのスキーマです。今どういうテーブルやカラムがあるかを見ることができます
```


