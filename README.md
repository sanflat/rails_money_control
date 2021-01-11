# Ruby on Rails お金管理アプリケーション

これは、次の教材で作られたサンプルアプリケーションを参考に作成しています。   
[*Ruby on Rails チュートリアル: 実例を使って Rails を学ぼう*](http://railstutorial.jp/)
[Michael Hartl](http://www.michaelhartl.com/) 著

## ライセンス

[Ruby on Rails チュートリアル](http://railstutorial.jp/)内にあるすべてのソースコードは
MIT ライセンスと Beerware ライセンスのもとに公開されています。
詳細は [LICENSE.md](LICENSE.md) をご覧ください。

## 使い方

このアプリケーションを動かす場合は、まずはリポジトリを手元にクローンしてください。
その後、Dockerを使って構築します。

docker-compose.yml を元にコンテナに必要なイメージを構築
```
$ docker-compose build
```

構築したイメージを元にコンテナを構築して起動
```
$ docker-compose up -d
```

コンテナ環境に入る
```
$ docker-compose exec app ash
```

データベース関係の準備
```
ash(コンテナ内)
 $ rails db:create
 $ rails db:migrate
 $ rails db:seed
```

http://localhost:3000 にアクセス！！！


# 一時停止
```
$ docker-compose stop
```
# 再起動
```
$ docker-compose start
```
# コンテナ削除
```
$ docker-compose down
```
詳しくは、
・[*Ruby on Rails チュートリアル*](http://railstutorial.jp/)
・(https://qiita.com/Moo_Moo_Farm/items/0d08da27371272ed1390)を参考にしてください。
