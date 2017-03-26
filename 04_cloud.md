# Cloudサービス

ここからはクラウドサービスを活用して、インターネット上にWebサーバを構築してみます。

以下のクラウドサービスが有名です。

+ [AWS（Amazon Web Services）](https://aws.amazon.com/jp/)
+ [GCP（Google Cloud Platform）](https://cloud.google.com/)
+ [Microsoft Azure](https://azure.microsoft.com/ja-jp/)

いずれもサービスが充実しており、またコストも控え目で利用しやすいものになっています。

## DigitalOcean

DigitalOceanはプログラマーに人気のクラウドサービスです。シンプルでかつ、プログラマブルなクラウドサービスです。

![](https://www.digitalocean.com/assets/media/logo-dfead9f9.png)

https://www.digitalocean.com/

アカウントを作成したら、3つの作業でクラウド上にLinuxサーバを構築できます。

+ OSを選ぶ
+ サイズを選ぶ
+ リージョンを選ぶ

![](https://www.digitalocean.com/assets/media/homepage/create-5fe2f870.gif)

以上で利用できます。

> 以降は学習目的でサーバを構築します。不要になったらすぐにサーバを削除できるのもクラウドサービスの魅力です。本格的にビジネスで運用する場合は、ネットワークやファイアウォールなど、セキュリティ設定を勉強しておくとようにしてください。つまり自己責任で！

### 参考

DigitalOceanでは、クラウドサーバを稼働する単位をDropletと呼びます。最大で10台まで起動できます。クラウドサーバの起動は概ね数分で完了します。サーバ起動が完了すると登録したアカウントにパスワードが記載されたメールが届きます。

```
Your new Droplet is all set to go! You can access it using the following credentials:

Droplet Name: itcaret-0x
IP Address: 139.59.108.xxx
Username: root
Password: xxxxxxxxxxxxxxxxxxxxxxxxxx

For security reasons, you will be required to change this Droplet’s root password when you login. You should choose a strong password that will be easy for you to remember, but hard for a computer to guess. You might try creating an alpha-numerical phrase from a memorable sentence (e.g. “I won my first spelling bee at age 7,” might become “Iwm#1sbaa7”). Random strings of common words, such as “Mousetrap Sandwich Hospital Anecdote,” tend to work well, too.

As an added security measure, we also strongly recommend adding an SSH key to your account. You can do that here: https://cloud.digitalocean.com/settings/security?i=5259b3

Once added, you can select your SSH key and use it when creating future Droplets. This eliminates the need for root passwords altogether, and makes your Droplets much less vulnerable to attack.

Happy Coding,
Team DigitalOcean
```

> 他にもパスワード認証ではなく、秘密鍵認証という方法もあります。ビジネスシーンでは秘密鍵認証を行うことがほとんどです。

### 研修で利用するクラウドサーバ

|Team|IP|
|:--|:--|
|Team 1|139.59.106.101|
|Team 2|139.59.106.197|
|Team 3|139.59.102.40|
|Team 4|139.59.102.117|
|Team 5|139.59.102.188|
|Team 6|139.59.250.118|
|Team 7|139.59.100.55|
|Team 8|139.59.108.143|
