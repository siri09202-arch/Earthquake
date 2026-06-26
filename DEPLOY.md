# GitHub Pagesへの公開ガイド

このガイドに従って、あなたのGitHubアカウントで地震情報テキストジェネレーターを公開できます。

## 📋 前提条件

- GitHubアカウント（無料でもOK）
- Git がインストールされていること（または GitHub Desktop を利用）

## 🚀 公開手順

### ステップ1: リポジトリを作成

1. GitHub.com にログイン
2. 右上の `+` アイコン → `New repository` を選択
3. 以下を設定：
   - **Repository name**: `earthquake-text-generator`（または好きな名前）
   - **Description**: `地震情報をSNS形式で生成・共有するWebアプリ`
   - **Public**: チェック
   - **README.md を追加**: スキップ（後でアップロードします）
4. `Create repository` をクリック

### ステップ2: ファイルをアップロード

#### 方法A: GitHub Web UI（最も簡単）

1. 新しく作成したリポジトリを開く
2. `Add file` → `Upload files` をクリック
3. 以下のファイルをドラッグ&ドロップ：
   - `index.html`
   - `README.md`
   - `LICENSE`
   - `CONTRIBUTING.md`
   - `.gitignore`

4. コミットメッセージを入力
   ```
   Initial commit: Add earthquake text generator
   ```
5. `Commit changes` をクリック

#### 方法B: コマンドライン

```bash
# リポジトリをクローン
git clone https://github.com/yourusername/earthquake-text-generator.git
cd earthquake-text-generator

# ファイルを配置（すべてのファイルをディレクトリにコピー）
cp index.html README.md LICENSE CONTRIBUTING.md .gitignore .

# Git に追加
git add .

# コミット
git commit -m "Initial commit: Add earthquake text generator"

# プッシュ
git push origin main
```

### ステップ3: GitHub Pages を有効化

1. リポジトリのページで `Settings` タブをクリック
2. 左のメニューから `Pages` をクリック
3. **Source** セクションで：
   - Branch: `main` を選択
   - Folder: `/ (root)` を選択
4. `Save` をクリック

### ステップ4: ページにアクセス

設定から数分後（最大5分程度）、以下のURLで公開されます：

```
https://yourusername.github.io/earthquake-text-generator
```

ブラウザで確認してみてください！

## ✅ 公開後の確認

1. **デモデータが表示される**: API が利用できない場合、デモデータが自動表示されます
2. **更新ボタンが機能する**: 「更新」ボタンをクリックして最新の地震情報が取得できるか確認
3. **フォーマット選択が機能する**: ドロップダウンメニューからフォーマットを変更できるか確認
4. **コピー機能が機能する**: テキストが正しくクリップボードにコピーされるか確認

## 📱 モバイルでの確認

スマートフォンのブラウザで以下のQRコードを読み込むか、URLを入力してモバイル表示を確認します：

```
https://yourusername.github.io/earthquake-text-generator
```

レイアウトが正しく表示されることを確認してください。

## 🔄 更新方法

ファイルを更新する場合は以下の手順で：

#### GitHub Web UIの場合
1. ファイルを開く
2. 右上の鉛筆アイコンをクリック（編集）
3. 変更を入力
4. `Commit changes` をクリック

#### コマンドラインの場合
```bash
# ローカルでファイルを編集

# 変更を Git に追加
git add .

# コミット
git commit -m "Update: [変更内容]"

# プッシュ
git push origin main
```

数秒後にサイトが自動更新されます。

## 🎨 カスタマイズ

### サイトタイトルの変更

`index.html` を編集：
```html
<title>地震情報テキストジェネレーター</title>
```

### 説明文の変更

`README.md` を編集してからコミット

### ヘッダーの色を変更

`index.html` の以下の部分を編集：
```html
<header class="bg-blue-600">
<!-- bg-blue-600 を bg-blue-700, bg-indigo-600 など色名に変更 -->
</header>
```

[Tailwind CSS カラーパレット](https://tailwindcss.com/docs/customizing-colors)で利用可能な色名を確認できます。

## ⚠️ トラブルシューティング

### ページが表示されない

1. **GitHub Pages が有効か確認**
   - Settings → Pages で Source が設定されているか確認
2. **リポジトリ名を確認**
   - URL は `https://yourusername.github.io/リポジトリ名` の形式
3. **キャッシュをクリア**
   - Ctrl+F5 (Windows) または Cmd+Shift+R (Mac)

### スタイルが反映されない

- キャッシュをクリアして再度アクセス
- GitHub Pages の再デプロイ待機（最大5分）

### APIが動作しない

- ブラウザコンソール（F12）でエラーを確認
- P2P地震情報APIのステータスを確認：https://www.p2pquake.net/
- インターネット接続を確認

### モバイルで表示がおかしい

- ブラウザの開発者ツールで `iPhone SE` など別のデバイスで確認
- Tailwind のレスポンシブクラスが正しく設定されているか確認

## 📊 ページビューの追跡（オプション）

GitHub Pages のアクセス統計を確認：
1. Settings → Pages
2. 下部の "GitHub Pages usage" を確認

## 🔐 セキュリティ

このプロジェクトはクライアント側で動作するため、以下の点に注意：

- ⚠️ **APIキーを含めない**: `index.html` には API キーが含まれません（公開APIを使用）
- ✅ **ユーザーデータは保存されない**: クライアント側で処理されるため、プライバシーは保護されます
- ✅ **HTTPSで自動配信**: GitHub Pages は HTTPS を強制

## 📈 さらに情報を得るには

- [GitHub Pages のドキュメント](https://docs.github.com/en/pages)
- [GitHub Desktop ガイド](https://docs.github.com/en/desktop)
- [Tailwind CSS ドキュメント](https://tailwindcss.com/docs)

## 🤝 サポート

質問やトラブルがあれば、リポジトリの Issues に投稿してください。

---

**公開成功をお祈りします！** 🎉
