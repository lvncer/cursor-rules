# Cursor Rules

Cursor エディタ用の開発ルール集です。効率的で一貫性のある開発を支援するためのベストプラクティスとガイドラインを提供します。

## 📋 概要

このプロジェクトは、Cursor エディタでの開発において以下を実現するためのルール集です：

- **一貫性のある開発**: 統一されたコーディング規約とベストプラクティス
- **効率的な作業**: 自動化されたワークフローとテンプレート
- **品質管理**: エラー防止と保守性の向上
- **知識共有**: チーム内での技術的決定の透明性

## 🗂️ ルール構成

### 🔄 常時適用ルール

- **[グローバルルール](/.cursor/rules/globals.mdc)** - 基本的な開発原則と実行フロー
- **[TODO 管理ルール](/.cursor/rules/todo.mdc)** - タスク管理とプロジェクト進行
- **[Next.js ベストプラクティス](/.cursor/rules/nextjs.mdc)** - Next.js 開発の標準規約
- **[技術スタック](/.cursor/rules/stacks.mdc)** - 使用技術とバージョン管理
- **[AI チャット履歴管理](/.cursor/rules/chat-history.mdc)** - AI 会話の記録と管理

### 🎨 ファイル種別ルール

- **[UI/UX 設計・実装ルール](/.cursor/rules/uiux.mdc)** - `.tsx`ファイル用の UI/UX 規約

### 📖 手動参照ルール

- **[テスト駆動開発(TDD)](/.cursor/rules/tdd.mdc)** - テスト主導の開発プロセス
- **[データベース設計ルール](/.cursor/rules/db.mdc)** - DB 設計と SQL 管理

## 🛠️ 技術スタック

### フロントエンド

- **React** + **Next.js** (Server Components)
- **TypeScript** (厳格モード)
- **Shadcn/ui** + **Tailwind CSS**
- **Clerk** (認証)

### バックエンド

- **Prisma** (ORM)
- **Supabase** (BaaS)
- **Server Actions** + **Zod** (フォーム処理)

### 開発ツール

- **ESLint** + **PostCSS**
- **Jest** + **React Testing Library** (テスト)
- **Cypress/Playwright** (E2E テスト)
- **Stripe** (決済)
- **Vercel** (デプロイ)

## 🔧 MCP (Model Context Protocol)

Cursor エディタとの統合機能：

- **file-system** - ファイルシステム操作
- **github**
- **Figma**
- **supabase**

### 設定方法

1. `.cursor/mcp.json`のパスを環境に合わせて修正
2. GitHub Personal Access Token を設定
3. Cursor エディタを再起動

## 📁 プロジェクト構造

```sh
cursor-rules/
├── .cursor/
│   ├── rules/               # 開発ルール集
│   │   ├── globals.mdc      # グローバルルール
│   │   ├── nextjs.mdc       # Next.jsルール
│   │   ├── stacks.mdc       # 技術スタック
│   │   ├── uiux.mdc         # UI/UXルール
│   │   ├── db.mdc           # データベースルール
│   │   ├── todo.mdc         # TODO管理
│   │   ├── chat-history.mdc # チャット履歴管理
│   │   └── tdd.mdc          # テスト駆動開発
│   └── mcp.json            # MCP設定
├── README.md               # このファイル
└── .gitignore.example      # Git除外設定例
```

## 🚀 使用方法

### 1. セットアップ

```bash
# プロジェクトをクローン
git clone <repository-url>
cd cursor-rules

# .gitignoreを設定（必要に応じて）
cp .gitignore.example .gitignore
```

### 2. Cursor 設定

1. Cursor エディタでプロジェクトを開く
2. `.cursor/mcp.json`のパスを環境に合わせて修正
3. 必要に応じて GitHub token を設定

### 3. ルールの活用

- 各ルールファイルは自動的に Cursor に読み込まれます
- 開発時に AI が適切なルールを参照して支援します
- 重要な決定や会話は自動的に履歴として保存されます
- テスト駆動開発で品質を確保しながら実装を進めます

## 📝 ルールの特徴

### 🎯 シンプル・簡潔

- 冗長な説明を排除
- 要点のみに絞った実用的な内容
- 素早い参照が可能

### 🔄 自動化

- TODO 管理の自動更新
- チャット履歴の自動保存
- 一貫性のあるファイル構造

### 🛡️ 品質保証

- テスト駆動開発による高品質コード
- エラー防止のためのチェックリスト
- コードレビューの自動化
- セキュリティベストプラクティス

## 🤝 貢献

ルールの改善や新しいルールの追加は歓迎します：

1. 既存ルールの改善提案
2. 新しい技術スタックへの対応
3. ワークフローの最適化

## 📄 ライセンス

このプロジェクトは MIT ライセンスの下で公開されています。

---

**開発効率と品質の向上を目指して** 🚀
