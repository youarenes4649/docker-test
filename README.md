# lambda ローカルテスト環境 by Docker outside of Docker

## 概要
- Dockerコンテナ上にLambdaをローカル実行するサンプルです。

## 動作環境
- Mac
- Docker -23.0.5

## 動作確認

```
# 作業ディレクトリで以下のコマンドを実行
git clone https://github.com/youarenes4649/docker-test.git

# Docker起動
docker compose up -d

# コンテナ内に移動し sam cli コマンドでテンプレートを呼び出す
sam init 

# テンプレートのディレクトリ(test)に移動 
cd test

# testディレクトリにあるtemplate.yamlのpythonを3.9から3.10に変更    
Runtime: python3.9 -> Runtime: python3.10

# app.py を修正しデバックしたくなったら以下のコマンドを実行
sam local invoke

```

## 勉強になったこと


## 参考URL
https://github.com/yasu-s/aws-sfn-local/blob/min/README.md
