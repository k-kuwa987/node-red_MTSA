# 基本的な使い方
初回は以下のコマンドでnode-redのコンテナとmtsaビルド用のコンテナが起動する。
２回目以降は`docker-compose up -d`のみでOK。

```
docker-compose build
docker-compose up -d
```

node-redはブラウザでhttp://localhost:1880/ にアクセスすることで利用可能。



## mtsaのビルド
mtsaをビルドする場合は以下のコマンドを実行する。

```
docker-compose exec mtsa cd mtsa/maven-root/mtsa && mvn install -Dmaven.test.skip=true
```

ビルドが完了するとmtsa-data/mtsa/maven-root/mtsa/target内にjarファイルが生成される。
