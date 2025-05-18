# Ubuntuリリースノート: https://wiki.ubuntu.com/Releases
# ベースイメージ:Ubuntu 24:04
FROM ubuntu:24.04

# パッケージのインストール時に対話的なプロンプトが表示されないように設定する
ENV DEBIAN_FRONTEND=noninteractive

# 必要なパッケージのインストール
RUN set -eux && \ 
    apt-get update && \
    apt-get install -y \
    # bashコマンド補完
    bash-completion \
    # treeコマンド
    tree \
    # 基本的な開発ツール
    build-essential \  
    # URLからデータを転送するためのツール
    curl \
    # バージョン管理システム
    git \
    # テキストエディタ  
    vim \
    # 圧縮ツール
    zip \  
    # 解凍ツール
    unzip \
    # 圧縮アーカイブツール
    tar \  
    # ファイル間の差分を表示するためのツール
    diffutils \
    # ファイルやディレクトリを検索するためのツール
    findutils \
    # ファイルを圧縮・解凍するためのツール
    gzip \
    # コマンドラインで使用するGitリポジトリビューア
    tig \
    # コマンドの実行ファイルの場所を表示するためのツール
    which && \ 
    # APTキャッシュのクリーンアップ
    apt-get clean && \
    # APTリポジトリのメタデータを削除してディスクスペースを節約
    rm -rf /var/lib/apt/lists/*

WORKDIR /workspace

ENV LANG=C.UTF-8

ENV DEVCONTAINER=true