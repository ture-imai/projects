# WSL / Linux ホームディレクトリの基本メモ

## ホームディレクトリの構成 (/home/sqr/)

### 触らないもの（ドットファイル/フォルダ）
- `.bashrc`, `.bash_logout`, `.profile` — シェルの設定ファイル
- `.ssh/` — SSH鍵（GitHubへの接続などに使用）
- `.claude/`, `.claude.json` — Claude Codeの設定
- `.cache/` — 各種ツールのキャッシュ
- `.local/` — ローカルにインストールしたツール等

※ `.`（ドット）で始まるものはシステムやツールが自動管理するもの。触らない。

### 自分で使うもの
- `projects/` — プロジェクト用フォルダ（この中で作業する）
- `test/` — テスト用フォルダ

## フォルダ構成の例

```
/home/sqr/
├── .bashrc 等（設定ファイル、触らない）
├── projects/          ← プロジェクトをまとめるフォルダ
│   ├── my-website/
│   ├── my-app/
│   └── practice/
└── test/              ← テスト用

## GitHubとの連携

### 新しいプロジェクトを作ってGitHubに紐付ける場合
```bash
cd ~/projects/my-app
git init
git remote add origin git@github.com:ユーザー名/my-app.git
```

### GitHubからプロジェクトを持ってくる場合
```bash
cd ~/projects
git clone git@github.com:ユーザー名/my-app.git
```

※ projects/ の中のプロジェクトフォルダが、それぞれ1つのGitHubリポジトリに対応する。

## その他
- WSL内（/home/sqr/ 以下）で作業する方がパフォーマンスが良い
- Windowsのデスクトップ（/mnt/c/...）にプロジェクトを置くとWSLからのアクセスが遅くなるので避ける
- `.claude.json.backup.*` は自動生成されるバックアップ。放置でOK
