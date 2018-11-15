NECモバイルバックエンド基盤: Docker Compose
===========================================

NEC モバイルバックエンド基盤 サーバ一式を Docker Compose で
起動するための定義ファイルです。

使い方
======

以下コマンドで全サーバを起動します。

    $ docker-compose up -d

ここで起動されるサーバは以下のものになります。

* MongoDB サーバ
* RabbitMQ サーバ
* fluentd サーバ
* BaaS API サーバ
* BaaS Console サーバ
* BaaS SSE Push サーバ
* BaaS Cloud Functions サーバ

停止する場合は以下の通りです。

    $ docker-compose stop
    
各サーバの URL は以下の通りです。

* api-server: http://localhost:8080/api/
* console-server: http://localhost:8081/console/
* ssepush-server: http://localhost:8082/ssepush/

MongoDB のデータは data volume に保存されます。

簡易版について
==============

simple/docker-compose.yml に簡易版の定義ファイルを用意しています。

こちらの定義ファイルでは、MongoDBサーバ、BaaS APIサーバ、BaaS Consoleサーバの
３つだけが起動されます。
