# git-study-group
Gitの勉強会におけるハンズオン用リポジトリ
実践を通して基本的なGit操作（Github操作も少し含む）を理解することを目的とする。

**前準備**

- gitのインストール
- Githubのアカウントを作る

## Case1. ローカルファイルのバージョン管理を開始する

- ローカルディレクトリを用意、適当なテキストファイルを用意
- git init
- git status
- git add .
- git status
- git commit -m "comment"


## Case2. ローカルリポジトリ→サーバーのリモートリポジトリへ

- Githubでリモートリポジトリを作る（まだない場合のみ）
- git remote add
- (git fetch, merge)
- git push (origin master)


## Case3. サーバーのリモートリポジトリ（自分の）→ローカルリポジトリ

- git clone XXXXX
- ファイルを編集
- git status
- git add (-u)
- git status
- git commit -m "comment"
- git push (origin master)


## Case4. サーバーのリモートリポジトリ（他人の）→ローカルリポジトリ

- git clone (他人のリポジトリ)


## Case5. サーバーのリモートリポジトリ（他人の）の編集に参加する

- 他人のリモートリポジトリをGithubでForkする
- git clone (Forkした自分のリポジトリ)
- 編集用のブランチを作成し、そちらのブランチに移動
- 空のコミット＋プッシュ＋プルリクエストを作成
  - git commit --allow-empty -m "initial"
  - git push origin (feature-branch)
  - (Github上)Forkした自分のリポジトリにプルリクエストを作成
  - Fork元の他人のリポジトリにプルリクエストを作成
  - 編集の内容などをコメントに記述
- ローカルリポジトリに戻ってファイルを編集
- git add -u
- git commit -m "comment"
- git push origin (feature-branch)
- (Github上)プルリクエストが更新されている
- ...

