# README #

## このリポジトリについて ##

[PHP公式](https://hub.docker.com/_/php/)のApache用イメージを元にMovable Typeを動かすのに必要なパッケージを追加したDockerイメージ構築用のリポジトリです。

今のところPHP公式の以下の3つのイメージを使用しています。

1. apache2.4系+PHP5.6系
1. apache2.4系+PHP7.4系
1. apache2.4系+PHP8.0系

これらに対してMovable Typeの稼働とメール処理に必要なパッケージを追加しています。前提条件などは以下のとおりです。

- RDBMSはMariaDB
- MTAはexim4
  - sendmailコマンドの利用が可能
  - すべてのメールは別コンテナの[mailhog](https://github.com/mailhog/MailHog)(1025/tcp)に転送

## 想定している環境など ##

Docker Composeで以下のコンテナを動かす想定です。

- apache+phpどれかor全部
- MariaDB
- [mailhog](https://github.com/mailhog/MailHog)

前述の通りexim4がすべてのメールをmailhogの1025/tcpに転送するように設定しているため、mailhog側の設定もそれに合わせてください。

※ 元々、自社のコンテンツ制作チームがMovable Typeでのサイト構築に加え、通知メールや[A-Form](https://www.ark-web.jp/movabletype/)やPHP製のメールフォームなどの動作検証も行うために構築したものなので「動けば良い」レベルです。あらかじめご了承ください。

## 追加で必要なもの ##

このリポジトリには以下に関する設定は含まれていません。利用する環境に合わせて準備・追加してください。

- apache
- PHP

---

## 何かありましたら… ##

@bsdmadまでご連絡ください。
