# GitHub Pagesでの公開手順

## ステップ1: GitHubリポジトリの作成

1. [GitHub](https://github.com) にログイン
2. 右上の「**+**」→「**New repository**」をクリック
3. リポジトリ名: `solitaire-game`（任意の名前でOK）
4. **Public** を選択
5. 「**Create repository**」をクリック

## ステップ2: コードのアップロード

### 方法A: Webインターフェースから（推奨・簡単）

1. 作成したリポジトリページで「**uploading an existing file**」をクリック
2. 以下のファイルをドラッグ&ドロップ：
   - `index.html`（ゲーム本体）
   - `README.md`（説明文書）
   - `DEPLOY.md`（このファイル）
   - `.gitignore`（Git設定）
3. 「**Commit changes**」をクリック

### 方法B: Git コマンドライン（上級者向け）

```bash
# リポジトリを初期化
git init
git add .
git commit -m "Initial commit: Solitaire game with mobile support"

# GitHubにプッシュ
git branch -M main
git remote add origin https://github.com/yourusername/solitaire-game.git
git push -u origin main
```

## ステップ3: GitHub Pagesの有効化

1. リポジトリページで「**Settings**」タブをクリック
2. 左メニューから「**Pages**」を選択
3. **Source** セクションで：
   - 「**Deploy from a branch**」を選択
   - Branch: 「**main**」を選択
   - Folder: 「**/ (root)**」を選択
4. 「**Save**」をクリック

## ステップ4: アクセス

数分後（通常1〜5分）、以下のURLでアクセス可能になります：

```
https://yourusername.github.io/solitaire-game/
```

※ `yourusername` はあなたのGitHubユーザー名に置き換えてください

### URLの確認方法

1. リポジトリの「**Settings**」→「**Pages**」を開く
2. 上部に表示される「**Your site is live at...**」でURLを確認
3. URLをクリックしてサイトにアクセス

## ステップ5: ファイルの更新方法

### Webインターフェースで更新

1. GitHubのリポジトリページで `index.html` をクリック
2. 右上の「**鉛筆マーク（Edit）**」をクリック
3. 内容を編集
4. 「**Commit changes**」をクリック
5. 1〜5分後に変更が反映されます

### 丸ごと置き換える場合

1. 古いファイルをクリック→「**ゴミ箱マーク**」で削除
2. 「**Add file**」→「**Upload files**」で新しいファイルをアップロード

## カスタムドメインの設定（オプション）

独自ドメイン（例：`www.example.com`）を使用する場合：

1. **Pages設定**で「**Custom domain**」に独自ドメインを入力
2. ドメインのDNS設定でCNAMEレコードを追加：
   ```
   CNAME  yourusername.github.io
   ```
3. 「**Enforce HTTPS**」にチェックを入れる（推奨）

通常は独自ドメインは不要なので、**空欄のまま**で問題ありません。

## トラブルシューティング

### ページが表示されない
- 5〜10分待ってから再度アクセス
- ブラウザのキャッシュをクリア（Ctrl+Shift+R / Cmd+Shift+R）
- リポジトリが **Public** になっているか確認

### 404エラーが出る
- `index.html` がリポジトリのルート（トップ）にあることを確認
- ファイル名が正確に `index.html`（小文字）であることを確認

### 変更が反映されない
- 1〜5分待つ（ビルドに時間がかかる場合があります）
- ブラウザのキャッシュをクリア
- シークレット/プライベートモードで確認

### iPhoneで動かない
- 最新版の `index.html` がアップロードされているか確認
- Safari以外のブラウザ（Chrome等）も試してみる

## よくある質問

**Q: 無料で使えますか？**  
A: はい、GitHub Pagesは完全無料です。

**Q: 商用利用できますか？**  
A: はい、可能です。

**Q: アクセス解析はできますか？**  
A: Google Analyticsなどを追加すれば可能です。

**Q: 独自ドメインは必要ですか？**  
A: いいえ、`username.github.io/solitaire-game/` で十分です。

## 次のステップ

1. ✅ ファイルをアップロード
2. ✅ GitHub Pagesを有効化
3. ✅ URLにアクセスして確認
4. 🎉 友達にシェア！

---

質問がある場合は、GitHubのIssuesで報告してください。
