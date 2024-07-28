# git-sandbox

# Rules

## Branch protection rules

1. `branch-protection-test*`にマッチするブランチは[保護ブランチ](https://docs.github.com/ja/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches)を設定している

## GitHub Project

[git-my-sandbox](https://github.com/users/priv-ts/projects/8/views/1)プロジェクトを使用する

### Issue 作成　~　プルリクエスト作成　~　 Close の基本的な流れ

1. Issue を起票する
2. Issue > Create a branch > Repository と Branch を選択
3. `git fetch origin`
4. `git checkout {ブランチ名}`
5. 修正/変更 > commit > Push
6. Pull Request (**このときに`close #{Issue番号}`を本文に指定する**)
7. Merge Pull Request

### ローカル環境で GitHub Actions を実行する(act)

- [WIP]GitHub 環境だとエラーとなってしまう
- [act を使って GitHub Actions をローカル実行する](https://zenn.dev/yumemi_inc/articles/203779a4eba922)
- 実行コマンド
  - `act pull_request --container-architecture linux/amd64`
