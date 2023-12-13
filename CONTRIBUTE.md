# 修正に際し

## 起動関連

``` bash

# まず削除
docker rm custom-keycloak

# イメージ化
docker image build -t custom-keycloak:v4.0.0 .
# バージョンタグをカウントアップもしくはイメージ削除する必要がある

# imageからコンテナ起動
docker run  -e KEYCLOAK_ADMIN=admin -e KEYCLOAK_ADMIN_PASSWORD=admin -p 8080:8080 --name custom-keycloak -it custom-keycloak:v4.0.0 start-dev
# バージョンはイメージと合わせたタグにする必要あり

```

## メール

sendgrid
HOST:smtp.sendgrid.net
PORT:25
ID:apikey
PW:
