# クラウドサーバへの接続

クラウドサーバに接続するには次の情報が必要です。

+ 接続ホスト（IPアドレス）
+ ユーザ名
+ パスワード（あるいは秘密鍵）

接続ホスト（IPアドレス）については、前の章で取得済みです。また、今回、ユーザ名はrootでログインできます。

> テキストはユーザ名がubuntuとなっています。rootに読み替えて進めます。パスワードは口頭でお伝えします。

以下、サーバのIPアドレスが52.79.97.23、ユーザ名がrootという前提で進めます。

クラウドサーバに接続するにはSSHプロトコルを使います。

## Macユーザ

「ターミナル」アプリケーションを起動して、以下のコマンドを入力します。

```
ssh root@52.79.97.23
```

## Windowsユーザ

WindowsにはMacの「ターミナル」のような、リモートサーバに接続する標準的なアプリケーションがありません。ここではTeraTermというアプリケーションをインストールしておきましょう。

以下のページにアクセスして、teraterm-4.89.zipをダウンロードします。

https://osdn.jp/projects/ttssh2/releases/64118

<img src="https://s3-ap-northeast-1.amazonaws.com/itcaret/itc_seminar/TT00.PNG" >


> ダウンロードしたzipファイルは任意のフォルダに解凍しておいてください。


TeraTermの起動手順は以下のとおりです。

1.HostにクラウドサーバのIPアドレス（52.79.97.23など）を入力して、OKボタンをクリックします。

<img src="https://s3-ap-northeast-1.amazonaws.com/itcaret/itc_seminar/TT01.PNG" >

2.初回接続時は、次のような警告が表示されますが、continueボタンをクリックします。

<img src="https://s3-ap-northeast-1.amazonaws.com/itcaret/itc_seminar/TT02.PNG" >

3.User nameにrootを入力してOKをクリックします。次のように表示されればクラウドサーバへの接続は完了です。

<img src="https://s3-ap-northeast-1.amazonaws.com/itcaret/itc_seminar/TT05.PNG" >


> 難しそうな黒い画面が表示されました。この画面の中での操作は、すべてクラウドサーバ上で実行されます。
