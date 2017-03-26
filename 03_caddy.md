# Webサーバのインストール

それでは実際にWebサーバを動作させてみましょう。本格的なWebサーバを構築するにはApacheやnginxがオススメですが、まずは使い方がシンプルなCaddyというサーバソフトウェアで実験してみましょう。

https://caddyserver.com/

![](https://s3-ap-northeast-1.amazonaws.com/itcaret/itc/img/webpg/day3/caddy3.png)

Caddyは次世代の通信プロトコルであるHTTP2.0をサポートする新鋭のWebサーバです。シンプルで使いやすいのも特徴の一つです。

## ダウンロード

以下のURLからWindowsやOS Xといったプラットフォームを選択してCaddyをダウンロードします。

https://caddyserver.com/download

### 追記2017/03/26

現行のWindows版のCaddy 0.9.5 は起動時にエラーメッセージが出るので、以下のリンクから0.9.4をダウンロードしてください。

[Windows 64bit]
https://github.com/mholt/caddy/releases/download/v0.9.4/caddy_windows_amd64.zip

[Windows 32bit]
https://github.com/mholt/caddy/releases/download/v0.9.4/caddy_windows_386.zip

## ファイルの解凍

ダウンロードしたZIPファイルを解凍すると次のようなフォルダが展開されるでしょう。

+ caddyフォルダ（caddy_darwin_amd64_customなど）
  + CHANGES.txt
  + LICENSES.txt
  + README.txt
  + caddy
  + init

> 以降はcaddyフォルダをデスクトップ上に配置するものとします。

上記のcaddyファイル（Windowsの場合はcaddy.exe）がサーバの起動ファイルです。caddyを起動するにはターミナル（コマンドプロンプト）を使用します。

ターミナルを起動したら解凍先フォルダに移動します。

```
cd 解凍先フォルダ（C:¥caddyなど）
```


Macの場合は、次のようにcaddyコマンドを実行します。

```
./caddy
```

Windowsの場合は、次のようにcaddyコマンドを実行します。

```
caddy.exe
```

次のようなメッセージが表示されるとCADDYは正常に起動しています。

```
Activating privacy features... done.
http://:2015
```

Caddyは2015番ポートで起動しているのがわかります。

> control + c を入力するとCaddyは停止します。


ブラウザから以下のURLにアクセスしてみましょう。

```
http://（IPアドレス）:2015
```

> アクセス対象のファイルが存在しないため404 Not Foundが表示されます。

![](https://s3-ap-northeast-1.amazonaws.com/itcaret/itc/img/webpg/day3/caddy1.png)

## 公開フォルダ（ドキュメントルート）

上記のとおり、Caddyを実行した場合、Caddyのデフォルトの公開フォルダは「caddyフォルダ（ZIPを解凍したフォルダ）」となります。公開フォルダにHTMLファイルを配置してみましょう。

> 公開フォルダに配置したコンテンツのみ、クライアントからアクセス可能となります。

以下のHTMLファイルを作成し、sample.htmlという名前でファイルを保存します。このとき保存先のフォルダを「caddyフォルダ（ZIPを解凍したフォルダ）」としてください。


```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Hello CADDY!</title>
  </head>
  <body>
    <h1>Hello CADDY!</h1>
  </body>
</html>
```

ブラウザから以下のURLにアクセスしてみましょう。

```
http://（IPアドレス）:2015/sample.html
```

![](https://s3-ap-northeast-1.amazonaws.com/itcaret/itc/img/webpg/day3/caddy2.png)

> ファイアウォールの設定などネットワーク環境にも依存しますが、通常はとなりの人のパソコン（Webサーバ）にもアクセスできます。
