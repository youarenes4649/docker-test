# docker compose up -d --build yamlファイルからイメージを作成し
# ベースイメージを指定 macがホストosの時は 前に--platform=linux/amd64 をつける
FROM --platform=linux/amd64 python:3.10


# 標準モジュール インストール
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    build-essential \
    git 

# sudo インストール
RUN apt update && \
    apt install sudo

# pip アップグレード
RUN pip install --upgrade pip

# requirements.txt のインストール

# AWS CLI インストール
RUN curl " https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
    unzip awscliv2.zip \
    sudo ./aws/install \
    rm awscliv2.zip

# SAM CLI インストール
RUN pip install awscli aws-sam-cli

CMD ["/bin/bash"]








