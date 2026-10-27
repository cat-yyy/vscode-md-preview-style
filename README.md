# Markdown Preview White

VS Code の Markdown プレビューを、テーマに関係なく **白背景・読みやすい装飾** で表示する自作拡張機能です。
`contributes.markdown.previewStyles` で `styles/preview.css` をプレビューに注入します。

## 装飾内容

- 白背景 + 濃いグレー文字、日本語フォント優先
- 見出しにアクセントライン（H1 下線 / H2・H3 左ライン）
- テーブル：角丸枠、ヘッダー背景、ゼブラストライプ、ホバー強調
- コードブロック：薄グレー背景 + GitHub Light 風シンタックスハイライト
- 引用 / GitHub アラート / タスクリスト / kbd / 脚注

## インストール

```powershell
npx @vscode/vsce package          # md-preview-white-0.1.0.vsix を生成
code --install-extension md-preview-white-0.1.0.vsix
```

または VS Code の拡張機能ビュー「…」→「VSIX からのインストール」。

WSL / Remote 接続時に効かない場合は、リモート側にも同じ VSIX をインストールしてください。

## カスタマイズ

`styles/preview.css` 冒頭の `:root` 変数（色・フォント）を変更 → `version` を上げて再パッケージ・再インストール。

## 確認

`sample.md` を開いて `Ctrl+Shift+V`（または `Ctrl+K V`）。
