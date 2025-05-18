# 操作コマンド一覧

## Docker の操作コマンド

### コンテナの一覧を表示する

```sh
docker ps -a
```

### Docker の未使用データをすべて削除する

```sh
sudo docker system prune -a
```

## Git の設定方法

### ユーザ名の設定

```sh
git config --global user.name "自身のユーザ名"
```

### メールアドレスの設定

```sh
git config --global user.email "自身のメールアドレス"
```

### git pull したときに、rebase を行う

```sh
git config --global pull.rebase true
```

### 直前のコミットを取り消す

```sh
git reset --soft HEAD^
git push --force-with-lease
```

### 特定のコミットまで戻す

`HEAD~2`と指定した場合は、最新のコミットから 2 つ前まで戻す

```sh
git reset --soft HEAD~2
git push --force-with-lease
```

## VSCode コマンド

"Ctrl + Shift + P"でコマンドパレット開き、各コマンドを実行する
