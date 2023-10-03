# 🐳

## 環境構築

### 1. 【docker-template】リポジトリをテンプレートとして、自身のGithubにリポジトリを作成する
<br>
<img width="1440" alt="スクリーンショット 2021-12-24 11 05 14" src="https://user-images.githubusercontent.com/63081802/147306983-b09827a5-cdbd-4061-a1c3-390496b266a8.png">

<br>
### 2. 【1で作成したリポジトリ】をローカル環境に複製する（cloneする）
<br>
```
git@github.com:tech-quest/docker-template.git
```

<br>
### 3. 【Dockerコンテナ】の起動
<br>
※ Docker Desktop を立ち上げてから以下のコマンドを実行しましょう。
<br>
（インストールがまだの方は、してください。）
<br>
※ 2でcloneしたリポジトリに移動してから以下のコマンドを実行しましょう。

```
./docker-compose-local.sh up
```

<br>
## ページ紹介

### php

[localhost:8080](http://localhost:8080)

### PHPMyAdmin

[localhost:3306](http://localhost:3306)

<br>
## よくある質問

### 作業の終了後は、どうすべきですか？

作業の終了後は、exit コマンドを実行してください。
<br>
exitと入力し、Enterを押すと、Dockerコンテナが停止します。
<br>
（再度、作業をする際は、もう一度コンテナの起動をしましょう。）

```
exit
```

<br>
### Dockerコンテナの起動をしようとしたらエラーになります。

他のコンテナが起動していてエラーになっている可能性があります。
<br>
Docker Desktopにて他のコンテナを停止してから再度コンテナの起動をすると解決するかもしれません。
<br>
<br>
上記でも解決しない場合は、一度PCを再起動してから、コンテナの起動をしましょう。
<br>
PCを再起動すると、コンテナがすべて停止します。

<br>
## その他

### Docker 環境に変更があった時

```
./docker-compose-local.sh up --build
```

## 設定を変更したい

```
localhost:8080をhtmlが表示されるようにしたい -> nginx/default.conf 4行目を index index.htmlにする。
```
