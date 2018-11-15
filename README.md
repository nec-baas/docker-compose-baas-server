NECモバイルバックエンド基盤: Docker Compose
===========================================

NEC モバイルバックエンド基盤 サーバ一式を Docker Compose で
起動するための定義ファイルです。

使い方
======

以下二種類の定義ファイルを用意しています。

* simple: MongoDB, BaaS API server, BaaS Console server
* full: simple に加え、RabbitMQ server, fluend server,
  SSE Push server, Cloud Functions server を含む

simple, full いずれかのディレクトリに移動し、以下コマンドで起動します。

    $ docker-compose up -d

停止する場合は以下の通りです。

    $ docker-compose stop
    
各サーバの URL は以下の通りです。

* api-server: http://localhost:8080/api/
* console-server: http://localhost:8081/console/
* ssepush-server: http://localhost:8082/ssepush/

MongoDB のデータは data volume に保存されます。
