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
- **[ワークフロー](/.cursor/rules/workflow.mdc)** - Issue 管理・Git 操作・PR 作成の統合フロー
- **[Next.js ベストプラクティス](/.cursor/rules/nextjs.mdc)** - Next.js 開発の標準規約
- **[技術スタック](/.cursor/rules/stacks.mdc)** - 使用技術とバージョン管理

### 🎨 ファイル種別ルール

- **[UI/UX 設計・実装ルール](/.cursor/rules/uiux.mdc)** - `.tsx`ファイル用の UI/UX 規約

### 📖 手動参照ルール

- **[テスト駆動開発(TDD)](/.cursor/rules/tdd.mdc)** - テスト主導の開発プロセス
- **[データベース設計ルール](/.cursor/rules/db.mdc)** - DB 設計と SQL 管理

## 🔧 MCP (Model Context Protocol)

Cursor エディタとの統合機能：

- **github** - GitHub 操作（Issue 作成・PR 管理）
- **Figma** - デザインファイル連携
- **supabase** - データベース操作

### 設定方法

1. `.cursor/mcp.json`のパスを環境に合わせて修正
2. GitHub Personal Access Token を設定
3. Cursor エディタを再起動

## 📁 プロジェクト構造

```sh
cursor-rules/
├── .cursor/
│   ├── prompts/
│   │   └── yyyymmdd_category.md    # 手動エクスポートしたプロンプトファイル
│   ├── rules/
│   │   ├── globals.mdc             # グローバルルール
│   │   ├── workflow.mdc            # 統合ワークフロー（Issue・Git・PR）
│   │   ├── nextjs.mdc              # Next.jsルール
│   │   ├── stacks.mdc              # 技術スタック
│   │   ├── uiux.mdc                # UI/UXルール
│   │   ├── db.mdc                  # データベースルール
│   │   └── tdd.mdc                 # テスト駆動開発
│   └── mcp.json                    # MCP設定
├── README.md
└── .gitignore.example
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

### 2. 個人用ルール設定（重要）

このプロジェクトをダウンロードした後、**個人用の環境設定ルール**を追加する必要があります：

#### Windows/PowerShell ユーザーの場合

1. **Cursor 設定を開く**: `Ctrl + ,` または右上の設定ボタン
2. **「Rules」**セクションに移動
3. **「User Rules」**に以下の内容を追加：

````markdown
## 基本環境

- **OS**: Windows 11
- **シェル**: PowerShell

## コマンド操作

### 必須ルール

- **PowerShell 使用必須**
- **Bash コマンド使用禁止**
- **Windows パス形式使用**

### 基本コマンド

```powershell
# ディレクトリ操作
Get-ChildItem, Set-Location, New-Item
# ファイル操作
New-Item, Remove-Item, Move-Item
# パッケージ管理
npm, yarn, pnpm (PowerShell経由)
```

## 禁止事項

- `ls`, `mkdir`, `cd`, `rm` 等の Bash コマンド
- `sudo` コマンド
- Linux/Mac 固有のパス指定

## 推奨事項

- Windows Terminal 使用
- 管理者権限が必要な場合は明示的に指示
- PowerShell コマンドレット優先使用
````

### 3. Cursor 設定

1. Cursor エディタでプロジェクトを開く
2. `.cursor/mcp.json`のパスを環境に合わせて修正
3. 必要に応じて GitHub token を設定

### 4. ルールの活用

- 各ルールファイルは自動的に Cursor に読み込まれます
- 開発時に AI が適切なルールを参照して支援します
- **GitHub Issue でタスク管理**し、一元的な進捗管理を実現
- テスト駆動開発で品質を確保しながら実装を進めます

### 5. 個人用ルールの重要性

**なぜ個人用ルールが必要？**

- **環境固有の設定**: OS・シェル・エディタの違いに対応
- **個人の好み**: コーディングスタイル・命名規則の統一
- **プロジェクト非依存**: 全プロジェクトで一貫した支援を受けられる
- **チーム協力**: 各メンバーが最適な環境で開発可能

**設定のコツ**:

- 簡潔で具体的なルールを記述
- 禁止事項を明確に指定
- 使用頻度の高いコマンドを優先的に記載

### 6. 開発ワークフロー

```bash
# 1. Issue作成（GitHub MCP使用）
# 2. ブランチ作成
git checkout -b feat/123-feature-name
# 3. フェーズごとの開発・コミット
# 4. PR作成（GitHub MCP使用）
# 5. レビュー・マージ
```

## 📝 ルールの特徴

### 🎯 シンプル・簡潔

- 冗長な説明を排除
- 要点のみに絞った実用的な内容
- 素早い参照が可能
- **1 つの統合ワークフローファイル**で完結

### 🔄 自動化

- Issue 管理の自動更新
- 一貫性のあるファイル構造
- MCP 活用による効率的な操作

### 🛡️ 品質保証

- **GitHub Issue による一元管理**（Single Source of Truth）
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
