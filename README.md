# 🌍 地震情報テキストジェネレーター

最新の地震情報をリアルタイムで取得し、20以上のフォーマットで自由に生成・コピーできるWebアプリケーションです。

## ✨ 機能

### 📡 リアルタイム地震情報
- P2P地震情報APIから最新の地震データを自動取得
- 最大震度3以上の国内地震と海外地震に対応
- 地震発生時刻、マグニチュード、震源地、津波情報をすべて表示

### 📝 複数フォーマット対応
20以上のフォーマットから選択可能：

**通常バージョン（市区町村単位）**
- 標準フォーマット
- Discord / X(Twitter) / LINE / Instagram / YouTube
- NHKニュース風 / Yahoo!天気・災害風 / 気象庁風
- ウェザーニュース風 / tenki.jp風
- J-RISQ / Yahoo!防災速報風 / P2P地震情報風
- 特務機関NERV風 / JQuake風 / EQMonitor風
- EarthQuickly風 / DPI-Bot風
- 簡易フォーマット / 詳細フォーマット

**観測点バージョン（詳細な地点情報）**
- 上記の各フォーマットに対応した観測点版

### 🎯 便利な機能
- ワンクリックでテキストをコピー可能
- 複数地震の履歴から選択可能
- モバイルフレンドリーなレスポンシブデザイン
- インターネット接続不要時はデモデータで動作

## 🚀 使い方

### ブラウザから直接利用
1. GitHub Pagesホストされたページを開く
2. ページが自動的に最新の地震情報を取得
3. 左側のリストから利用したい地震を選択
4. 上部のドロップダウンメニューで出力形式を選択
5. 「コピーする」ボタンでテキストをクリップボードにコピー
6. SNSやチャットに貼り付け

### ローカルで実行
```bash
# このリポジトリをクローン
git clone https://github.com/yourusername/earthquake-text-generator.git
cd earthquake-text-generator

# ローカルサーバーを起動（Python）
python3 -m http.server 8000

# または Node.js
npx http-server

# http://localhost:8000 をブラウザで開く
```

## 📊 API情報

### 使用しているAPI
**P2P地震情報 API** (`https://api.p2pquake.net/v2/history`)

無料で利用可能な公開API。商用利用も可能です。

### 対応する地震情報
- 各地の震度に関する情報（DetailScale）：最大震度3以上
- 遠地地震に関する情報（Foreign）：すべて

### 震度スケール
- 1, 2, 3, 4, 5弱, 5強, 6弱, 6強, 7

## 🛠️ 技術スタック

- **フロントエンド**: Vanilla JavaScript
- **UI Framework**: Tailwind CSS
- **アイコン**: Font Awesome 6.0
- **API**: P2P地震情報 API v2
- **ホスティング**: GitHub Pages

## 📱 ブラウザ対応

- Chrome/Edge（最新版）
- Firefox（最新版）
- Safari（最新版）
- モバイルブラウザ対応

## ⚙️ プロジェクト構成

```
.
├── index.html          # メインアプリケーション
├── README.md           # このファイル
├── .gitignore          # Git設定ファイル
└── LICENSE             # ライセンス情報
```

## 🌐 GitHub Pagesでの公開

### 初回セットアップ

1. このリポジトリをフォーク

2. リポジトリ設定を変更
   - Settings → Pages
   - Source: `main` ブランチの `/root` フォルダを選択
   - Save をクリック

3. 数分後、以下のURLからアクセス可能
   ```
   https://yourusername.github.io/earthquake-text-generator
   ```

### 継続的な更新
`index.html` を編集して、変更をコミット・プッシュするだけでサイトが自動更新されます。

## 📝 カスタマイズ

### 色設定の変更
`index.html` の `<style>` セクションで震度ごとの背景色を編集可能：

```css
.shindo-5- { background-color: #ed8936; }  /* 5弱 */
.shindo-6-plus { background-color: #c53030; }  /* 6強 */
```

### フォーマット追加
`generateText()` 関数内に新しい `else if (format === 'カスタム名')` ブロックを追加

## ⚠️ 注意事項

- APIの可用性に依存：APIが利用できない場合はデモデータで動作
- CORS対応：ブラウザからのクロスオリジンリクエストに対応した環境が必要
- リアルタイムデータ：地震情報の更新には数秒～数分のタイムラグが発生する場合があります

## 🤝 コントリビューション

改善提案やバグ報告は、Issues/Pull Requestsで受け付けています。

1. このリポジトリをフォーク
2. フィーチャーブランチを作成 (`git checkout -b feature/amazing-feature`)
3. 変更をコミット (`git commit -m 'Add amazing feature'`)
4. ブランチにプッシュ (`git push origin feature/amazing-feature`)
5. Pull Requestを作成

## 📄 ライセンス

このプロジェクトはMITライセンスの下で公開されています。

## 📚 参考リンク

- [P2P地震情報 - API仕様](https://www.p2pquake.net/)
- [気象庁 - 地震情報](https://www.jma.go.jp/jma/index.html)
- [Tailwind CSS ドキュメント](https://tailwindcss.com/)
- [Font Awesome アイコン](https://fontawesome.com/)

## 💡 今後の予定

- [ ] 過去の地震履歴の保存機能
- [ ] カスタムフォーマットの作成機能
- [ ] 複数地震の一括出力
- [ ] ダークモード対応
- [ ] 多言語対応

## 🐛 既知の問題

- iOS SafariでのExecuteCommand実行時に稀にエラーが発生する場合があります
- APIレート制限に達した場合、自動的にデモデータが表示されます

---

**最終更新**: 2026年6月26日  
**作成者**: Your Name  
**リポジトリ**: https://github.com/yourusername/earthquake-text-generator
