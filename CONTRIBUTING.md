# コントリビューション ガイドライン

このプロジェクトへのコントリビューションをありがとうございます！以下のガイドラインに従ってください。

## 📋 コードスタイル

### JavaScript
- `var` ではなく `let` / `const` を使用
- セミコロンは必須
- インデントは2スペース
- 関数名はキャメルケース（`camelCase`）

### HTML/CSS
- インデントは2スペース
- クラス名はケバブケース（`kebab-case`）
- ID名は避け、できるだけクラスを使用

### コメント
```javascript
// 単一行コメント

/* 
 * 複数行コメント
 * わかりやすく説明する
 */
```

## 🔄 Pull Request プロセス

1. **フォーク**: リポジトリをフォーク
2. **ブランチ作成**: 意味のあるブランチ名で新しいブランチを作成
   ```bash
   git checkout -b feature/add-new-format
   git checkout -b fix/api-error-handling
   git checkout -b docs/update-readme
   ```
3. **変更**: コードを編集
4. **テスト**: ブラウザで動作確認
5. **コミット**: わかりやすいコミットメッセージで
   ```bash
   git commit -m "Add new earthquake format: NHK News style"
   ```
6. **プッシュ**: ブランチをプッシュ
   ```bash
   git push origin feature/add-new-format
   ```
7. **Pull Request**: GitHubでPRを作成し、詳細を記入

## 📝 PR タイトル の書き方

形式: `[Type] Description`

**Type の例**：
- `[Feature]` 新機能追加
- `[Fix]` バグ修正
- `[Docs]` ドキュメント更新
- `[Refactor]` コード整理（機能変更なし）
- `[Performance]` パフォーマンス改善

**例**：
```
[Feature] Add weather news format
[Fix] Resolve API timeout issue on slow networks
[Docs] Update installation instructions
```

## 🐛 バグレポート

Issues で報告する際は、以下を含めてください：

```markdown
## 概要
[簡潔な説明]

## 再現手順
1. ...
2. ...
3. ...

## 期待される動作
[何が起こるべきか]

## 実際の動作
[実際に何が起こったか]

## 環境
- OS: [Windows 11 / macOS 12 / Ubuntu 22.04 など]
- ブラウザ: [Chrome 120 / Firefox 121 など]
- その他: [重要な環境情報があれば]

## スクリーンショット
[あれば追加]
```

## ✨ 新機能のリクエスト

以下のテンプレートでIssueを作成してください：

```markdown
## 概要
[新機能のアイデア]

## メリット
[この機能があるとどの点が改善されるか]

## 実装案
[可能であれば実装方法を提案]

## 関連情報
[参考資料やリンクがあれば]
```

## 🎯 コントリビューションのアイデア

以下の領域でのコントリビューションを特に歓迎します：

- 新しい地震情報フォーマットの追加
- UI/UXの改善
- バグ修正
- ドキュメントの改善
- ローカライゼーション対応
- パフォーマンス最適化

## 📚 ローカル開発環境の構築

```bash
# リポジトリをクローン
git clone https://github.com/yourusername/earthquake-text-generator.git
cd earthquake-text-generator

# ローカルサーバーを起動
python3 -m http.server 8000
# または
npx http-server

# http://localhost:8000 でアクセス
```

## 🔍 テストしてから提出

- [ ] ブラウザで動作確認（Chrome, Firefox, Safari）
- [ ] モバイルでの表示確認
- [ ] コンソールにエラーがないか確認
- [ ] 新しい地震データフォーマットは複数パターンで検証

## 📖 コミットメッセージのガイドライン

```
[Type] Short summary (50 chars or less)

More detailed explanation if necessary. Wrap at 72 characters.
Explain what and why, not how.

- Bullet points are okay
- Reference issues: Fixes #123
```

## ❓ 質問がある場合

- Issue を作成して質問タグをつける
- Discussions を利用
- 既存のIssuesを検索（重複を避けるため）

## 🙏 謝辞

このプロジェクトに貢献してくれるすべての人に感謝します！

---

**最後に**: 楽しみながらコードを書いてください。質問や不確かな点があれば、遠慮なく聞いてくださいね！
