
## Docker install
### Mac
1.  [Docker for Mac](https://docs.docker.com/docker-for-mac/install/)からインストール
2. 正しくインストールされているか確認する

 ```command
docker version
```


# 基本構文

## Dockerfile 命令文
|｛命令｝|用途|
| --- |---  |
|FROM|元となるDockerイメージの指定|
|MAINTAINER|作成者の情報|
|RUN|コマンドの実行|
|ADD|ファイル／ディレクトリの追加|
|CMD|コンテナーの実行コマンド 1|
|ENTRYPOINT|コンテナーの実行コマンド 2|
|WORKDIR|作業ディレクトリの指定|
|ENV|環境変数の指定|
|USER|実行ユーザーの指定|
|EXPOSE|ポートのエクスポート|
|VOLUME|ボリュームのマウント|


# 注意点

# 参照プラグイン
[com.palantir.docker](https://plugins.gradle.org/plugin/com.palantir.docker)

