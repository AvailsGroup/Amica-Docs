# 第1章 - はじめに - Docker 

ここではDockerを使用した開発環境の建て方を説明します。

慣れている方はこっちのほうが楽だと思います。

- [第1章 - はじめに - Docker](#第1章---はじめに---docker)
  - [環境](#環境)
  - [構築方法](#構築方法)
    - [プロジェクトをクローンする](#プロジェクトをクローンする)
    - [ビルド](#ビルド)
    - [マイグレート](#マイグレート)
    - [JS関連ファイルをダウンロード](#js関連ファイルをダウンロード)
    - [credentialsとmasterkeyを再生成](#credentialsとmasterkeyを再生成)
    - [起動](#起動)
    - [コマンドの実行](#コマンドの実行)
    - [停止](#停止)
  


## 環境 

想定する環境は以下です。

- Windows

- WSL2 Ubuntu 20.04 LTS

- DockerDesktop

DockerDesktopとWSL2を事前に連携してください。

## 構築方法

### プロジェクトをクローンする

```bash
git clone https://github.com/Avails-Group/Amica
cd Amica
```

### ビルド

```bash
sudo docker-compose build
```

### マイグレート

```bash
sudo docker-compose run app rails db:create db:migrate
```

### JS関連ファイルをダウンロード

```bash
sudo docker-compose run app yarn install
```

### credentialsとmasterkeyを再生成

```bash
rm config/credentials.yml.enc
rm config/master.key
docker-compose run -e EDITOR=vim app rails credentials:edit
```

### 起動

```bash
#普通に起動
docker-compose up
# バックグラウンドで起動
docker-compose up -d
```

### コマンドの実行

```bash
docker-compose run app コマンド

#例 ルーティングの取得
docker-compose run app rails routes
```

### 停止

```bash
docker-compose down
```