# Webサーバのインストール

続いてWebページを配信するために、Webサーバをインストールしてみます。Webサーバ製品もいくつかありますが、ここでは世界中で最もよく利用されているApacheを利用します。

## クラウドサーバを最新化

クラウド上に作成してすぐのサーバは最新の状態になっていないので、以下のコマンドを使ってサーバの利用するソフトウェアを最新にしておきます。

```
apt-get update -y
```

## Webサーバ（Apache）のインストール

サーバ上にApacheをインストールします。Apacheは世界で最も使われているWebサーバープロダクトです。

> Apacheをインストールするとブラウザから http://52.79.97.23/ でアクセスできるようになります。

```
apt-get install apache2
```

### Apacheの起動と停止

Apacheは以下のコマンドで起動できます。

```
service apache2 start
```

停止するときは以下のようにコマンドを実行します。

```
service apache2 stop
```

## HTMLファイルのアップロード

手元のパソコンから、クラウド上にあるサーバにHTMLファイルをアップロードします。

### Macユーザの場合

Desktop上のsample.htmlをアップロードする場合は以下のように入力します。

```
scp /Users/murayama/Desktop/sample.html root@52.79.97.23
```

> 画像ファイルなどもアップロードできます。

### Windowsユーザの場合

起動中のTeraTermにアップロードしたいファイルをドラッグアンドドロップします。


## Apacheの公開フォルダにHTMLファイルをコピー

Apacheは標準で /var/www/html フォルダ上のファイルをWeb上に公開します。HTMLファイルを/var/www/htmlにコピーしましょう。

```
cp /root/sample.html /var/www/html
```

以上でLinuxサーバのセットアップは完了です。

## 動作確認

ブラウザを開いて、以下のURLにアクセスしてみましょう。

```
http://52.79.xx.xx/sample.html
```

作成したHTMLファイルを閲覧できれば完了です。

> 手元のスマートフォンからHTMLファイルを見ることもできます。
