# Git & GitHub の使い方メモ

## ファイルを変更したら GitHub に反映する手順

```bash
cd ~/projects
git add ファイル名
git commit -m "変更内容のメモ"
git push
```

## よく使うコマンド

| コマンド | 説明 |
|---------|------|
| `git status` | 変更されたファイルを確認 |
| `git add .` | すべての変更をステージング |
| `git add ファイル名` | 特定のファイルだけステージング |
| `git commit -m "メッセージ"` | 変更を記録 |
| `git push` | GitHub にアップロード |
| `git pull` | GitHub から最新を取得 |
| `git log --oneline` | コミット履歴を確認 |

## 例：memo.md を編集して GitHub に反映する

```bash
cd ~/projects
git add memo.md
git commit -m "memo.md を更新"
git push
```
