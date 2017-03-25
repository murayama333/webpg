# インターネットの仕組み

インターネットによるデータ通信は、主にHTTPとTCP/IPという2つの通信ルールで構成されています。

なぜ通信ルールは2つあるのでしょうか？HTTPとTCP/IPは階層構造になっています。

<img src="https://s3-ap-northeast-1.amazonaws.com/itcaret/itc/img/webpg/day3/tcpip.png" width="500px">

現実世界の交通網に例えるなら、TCP/IPは、信号や住所のようなもので、HTTPは宅急便のようなものです。

## TCP/IP

TCP/IPとはHTTPより低いレイヤーで動作する通信プロトコルで、インターネットの基盤となっています。TCP/IPではIPアドレスとポート番号の2つを管理しています。

### IP

IPはインターネットに接続されたコンピュータを識別する仕組みです。IPアドレスによってルーティングをサポートします。

IPアドレスとはネットワーク上にコンピュータに割り当てられた番号です。192.168.0.1のように、4つの数字で表現されます。IPアドレスがわかれば通信先のコンピュータを特定できます。

#### IPアドレスの調べ方

MacやLinuxの場合はターミナルを開いて以下のコマンドを入力します。

```
ifconfig
```

Windowsの場合はコマンドプロンプトを開いて以下のコマンドを入力します。

```
ipconfig
```

### TCP

TCPは信頼性のあるデータ通信を実現しています。大きなデータを効率よく送信するために分割したり、データが正しく送信されたかどうか確認する仕組みを持っています。

TCPはポート番号によって通信を識別しています。ポート番号とは、通信の必要なプログラムに割り当てられた番号です。1台のコンピュータの中では複数のプログラムが同時に動作しているので、どのプログラムにデータを渡すのかを指定するためにポート番号を使います。

> HTTPサーバは80番ポート、SSHサーバは22番ポートというように有名なプログラムは、標準で使うポート番号というのが決まっています。このようなポート番号をウェルノウンポートと呼びます。


## HTTP

Webサーバはネットワーク上でデータをやりとりする際、HTTPという通信プロトコルを使います。プロトコルとは「ルール」や「取り決め」を意味する言葉です。HTTPには以下のようなルールがあります。

+ クライアント（＝ブラウザなど）が要求データを送り、サーバが応答データを返す。通信は必ずクライアントからスタートする。
+ ネットワーク上を流れるデータは、一部を除いてほとんどがテキスト形式のデータである。人間が読んでも解析しやすい。
+ TCP/IPという通信ルールの上で動作する。


## Webサーバ

WebサーバとはHTMLやCSS、画像ファイルといったコンテンツをインターネット上に公開するソフトウェアです。Webサーバ上に公開されたコンテンツは、ブラウザから簡単にアクセスすることができます。

ブラウザとWebサーバはHTTPという通信ルールでデータのやりとりをしています。WebサーバはHTTPサーバとも呼ばれます。

ブラウザにChromeやFirefox、SafariといったソフトウェアがあるようにWebサーバにも代表的なソフトウェアがいくつかあります。

+ Apache
  + オープンソースのWebサーバソフトウェア。古くからの利用実績があり、No.1のシェアと言われている。
  + https://httpd.apache.org/
+ nginx
  + オープンソースのWebサーバソフトウェア。後進のWebサーバであり、シンプルで高速な実装となっている。
  + https://nginx.org/en/
+ IIS
  + Microsoft社が開発しているWebサーバソフトウェア。Windowsサーバ上で動作する。
  + https://www.iis.net/


## 公開フォルダ（ドキュメントルート）

Webサーバには公開フォルダと呼ばれる仕組みが用意されています。公開フォルダに配置したコンテンツ（HTMLなど）がWeb上に公開されるようになります。

![](https://s3-ap-northeast-1.amazonaws.com/itcaret/itc/img/webpg/day3/http.png)

公開フォルダはドキュメントルートなどと呼ばれます。