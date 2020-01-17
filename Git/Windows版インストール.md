# Windows版のGit設定

自分がWindowsユーザーじゃないため手こずった

## 利用ツール
VSCode

### 拡張機能
GitLens

## Gitクライアントのインストール
[Git for windows - Downloading Package](https://git-scm.com/download/win)

## Git Bushの起動


## Gitの初期設定をする
```
git config --global user.name "ユーザー名"
git config --global user.email "メールアドレス"
```

## ローカルリポジトリの作成
使用するのはVSCodeとする
- [ファイル] > [開く] > Gitで管理したいファイルがある場所のフォルダ
- VSCodeで`git init`で初期化
```
$ git init
```

## リモートリポジトリの作成
- Githubにリモートリポジトリの作成


## 秘密鍵・公開鍵を作成する
- `Git Bash`を起動
- コマンドの存在確認
```
which ssh-keygen
```
- 秘密鍵と公開鍵作成
キーの格納用フォルダ作成
```
$ mkdir ~/.ssh && cd ~/.ssh
```
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com" -f ~/.ssh/github_rsa
```

## ホスト設定

```
vi ~/.ssh/config
```

```
Host github.com
  HostName github.com
  IdentityFile ~/.ssh/github_rsa #先程作成した鍵のファイル名
  User git
```

## Github側の設定
- アカウントの[setting]>[SSH keys and GPG keys]>[New SSH Key]
- Titleに任意の名前と、Keyに作成した.pubの中身を貼り付ける
  - 今回はgithub_rsa.pubになる
