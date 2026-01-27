# GitHub Pagesへのデプロイ手順

## 必要なもの
- GitHubアカウント
- Git（インストール済みであること）

## 手順

### ステップ1: GitHubでリポジトリを作成

1. [GitHub](https://github.com) にログイン
2. 右上の「+」→「New repository」をクリック
3. リポジトリ情報を入力:
   - Repository name: `solitaire-game`（任意の名前）
   - Description: `クロンダイクソリティアゲーム`
   - Public を選択
4. 「Create repository」をクリック

### ステップ2: ローカルでファイルを準備

```bash
# 作業ディレクトリを作成
mkdir solitaire-game
cd solitaire-game

# Gitを初期化
git init

# index.html をこのフォルダにコピー
# （ダウンロードした index.html をここに配置）

# READMEもコピー（オプション）

# ファイルをステージング
git add .

# コミット
git commit -m "🎴 Initial commit: ソリティアゲームを追加"
```

### ステップ3: GitHubにプッシュ

```bash
# リモートリポジトリを追加（YOUR_USERNAMEを自分のユーザー名に変更）
git remote add origin https://github.com/YOUR_USERNAME/solitaire-game.git

# ブランチ名をmainに設定
git branch -M main

# プッシュ
git push -u origin main
```

### ステップ4: GitHub Pagesを有効化

1. GitHubのリポジトリページを開く
2. 「Settings」タブをクリック
3. 左メニューから「Pages」を選択
4. 「Build and deployment」セクションで:
   - **Source**: Deploy from a branch
   - **Branch**: main
   - **Folder**: / (root)
5. 「Save」をクリック

### ステップ5: デプロイ完了を確認

- 数分後、緑色のチェックマークが表示されます
- URLが表示されます: `https://YOUR_USERNAME.github.io/solitaire-game/`
- このURLをクリックしてゲームが表示されることを確認

## カスタムドメインの設定（オプション）

独自ドメインを持っている場合:

1. GitHub Pages設定で「Custom domain」に自分のドメインを入力
2. DNSプロバイダーで以下のレコードを追加:
   ```
   Type: CNAME
   Name: www (または任意のサブドメイン)
   Value: YOUR_USERNAME.github.io
   ```

## トラブルシューティング

### 404エラーが表示される
- ファイル名が `index.html` であることを確認
- GitHub Pagesが有効になっているか確認
- デプロイに数分かかることがあるので、少し待ってから再度アクセス

### ページが更新されない
- ブラウザのキャッシュをクリア（Ctrl+Shift+R または Cmd+Shift+R）
- GitHub Actionsのデプロイが完了するまで待つ

### iPhoneで表示が崩れる
- Safariで開いていることを確認
- ホーム画面に追加して全画面モードで使用

## 更新方法

ゲームを更新した場合:

```bash
# ファイルを更新後
git add .
git commit -m "🎨 デザインを改善"
git push
```

数分後、変更が自動的に反映されます。

---

## 完成！

これであなたのソリティアゲームがインターネット上で公開されました！
URLを友達や家族と共有して楽しんでください 🎉
