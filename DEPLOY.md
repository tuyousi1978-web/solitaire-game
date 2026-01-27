# GitHub Pagesでの公開手順

## ステップ1: GitHubリポジトリの作成

1. GitHubにログイン
2. 右上の「+」→「New repository」をクリック
3. リポジトリ名: `solitaire-game`（任意）
4. Public を選択
5. 「Create repository」をクリック

## ステップ2: コードのアップロード

### 方法A: Webインターフェースから

1. 作成したリポジトリページで「uploading an existing file」をクリック
2. `index.html`、`README.md`、`.gitignore` をドラッグ&ドロップ
3. 「Commit changes」をクリック

### 方法B: Git コマンドライン

```bash
git init
git add .
git commit -m "Initial commit: Solitaire game"
git branch -M main
git remote add origin https://github.com/yourusername/solitaire-game.git
git push -u origin main
```

## ステップ3: GitHub Pagesの有効化

1. リポジトリページで「Settings」タブをクリック
2. 左メニューから「Pages」を選択
3. Source: 「Deploy from a branch」を選択
4. Branch: 「main」を選択、フォルダは「/ (root)」を選択
5. 「Save」をクリック

## ステップ4: アクセス

数分後、以下のURLでアクセス可能になります：
```
https://yourusername.github.io/solitaire-game/
```

## カスタムドメインの設定（オプション）

独自ドメインを使用する場合：
1. Pages設定で「Custom domain」に独自ドメインを入力
2. DNS設定でCNAMEレコードを追加

## トラブルシューティング

- **ページが表示されない**: 数分待ってから再度アクセス
- **404エラー**: `index.html`がルートディレクトリにあることを確認
- **変更が反映されない**: ブラウザキャッシュをクリア（Ctrl+Shift+R）
