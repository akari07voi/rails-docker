# README

本アプリケーションを稼働させるために必要なステップは以下の通り。

## git clone を行って本リポジトリをローカルにクローンする
- git clone cloneURL

## ローカルリポジトリにクローン後、以下のコマンドでDockerImageの作成を行う

```
$ docker-compose build
```

## ローカル用のDBを作成する
```
$ docker-compose run web rake db:create
```

## docker-compose up でコンテナを起動する
```
＄ docker-compose up
```

## localhost:3000 で接続してPendingMigrationErrorと表示される場合は以下のコマンドを実行する
```
$ docker-compose run web rake db:migrate
```

## localhost:3000 で再度アクセスして正しくアクセスできれば起動完了です
