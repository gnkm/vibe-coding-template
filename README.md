# Vibe Coding Template

バイブコーディングを補助するためのテンプレートリポジトリ

## 前提条件

- [Cursor IDE](https://cursor.com/)
- [lefthook](https://github.com/evilmartians/lefthook) - Git Hooks 管理
- [gitleaks](https://github.com/gitleaks/gitleaks) - シークレット検出
- [osv-scanner](https://github.com/google/osv-scanner) - 脆弱性スキャン（オプション）

## セットアップ

### 1. テンプレートからリポジトリを作成

GitHub の「Use this template」ボタンをクリックして、新しいリポジトリを作成します。

### 2. 依存ツールのインストール

```bash
# macOS (Homebrew)
brew install lefthook gitleaks osv-scanner
```

### 3. Git Hooks の有効化

```bash
lefthook install
```

## ワークフロー

以下の順序で開発を進めることを推奨します。

### Step 1: PRD（要求仕様書）作成

`docs/prd_org.md` などに要求仕様書の草稿を保存し、以下を実行します。

```
/prd @docs/prd_org.md を参考にしてください。
```

出力: `docs/prd.md`

### Step 2: 技術選定

```
/tech-stack
```

出力: `docs/tech_stack.md`

### Step 3: 設計

```
/architecture
```

出力: `docs/architecture.md`

### Step 4: 実装計画作成

```
/plan
```

出力: `docs/plan.md`

### Step 5: プロトタイプ開発

```
/develop
```

### Step 6: 機能追加・修正

計画外の機能追加や修正を行う場合に使用します。

```
/start xxx機能を追加してください。
```

### Step 7: テスト

テストの作成・実行を行います。

```
/test ログイン機能のテストを作成してください
/test --smoke
```

### Step 8: Git コミット

```
/commit
```

## テンプレート構造

```
.
├── .cursor/
│   ├── commands/          # Cursor スラッシュコマンド定義
│   │   ├── prd.md         # /prd コマンド
│   │   ├── tech-stack.md  # /tech-stack コマンド
│   │   ├── architecture.md # /architecture コマンド
│   │   ├── plan.md        # /plan コマンド
│   │   ├── develop.md     # /develop コマンド
│   │   ├── start.md       # /start コマンド
│   │   ├── test.md        # /test コマンド
│   │   ├── commit.md      # /commit コマンド
│   │   └── assets/        # テンプレートファイル
│   └── rules/             # Cursor ルール設定
├── .claude/
│   └── skills/            # Claude 向けスキル定義
│       ├── frontend-design/  # フロントエンドデザインスキル
│       └── skill-creator/    # スキル作成スキル
├── AGENTS.md              # AI エージェント向けコンテキスト
├── CONTRIBUTING.md        # 開発ガイド
└── lefthook.yml           # Git Hooks 設定
```

## カスタマイズ

### コマンドのカスタマイズ

`.cursor/commands/` 内のファイルを編集して、プロジェクトに合わせたコマンドにカスタマイズできます。

### テンプレートのカスタマイズ

`.cursor/commands/assets/` 内のテンプレートファイルを編集して、出力形式を調整できます。

### スキルの追加

`.claude/skills/` に新しいスキルディレクトリを作成し、`SKILL.md` を配置することで、Claude 向けのスキルを追加できます。

## 関連ドキュメント

- [CONTRIBUTING.md](CONTRIBUTING.md) - 開発ガイド（ブランチ命名規則、コミットメッセージ規約など）
- [AGENTS.md](AGENTS.md) - AI エージェント向けコンテキスト

## ライセンス

[LICENSE](LICENSE) を参照してください。
