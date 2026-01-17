# 開発ガイド (Development Guide)

## 開発フロー

### ブランチの命名規則

ブランチ名は、変更の種類とその内容がわかるように、以下の形式で命名してください。

`prefix/branch-name`

推奨される Prefix:
- `feature/`: 新機能の追加 (例: `feature/add-settings-ui`)
- `fix/`: バグ修正 (例: `fix/audio-capture-error`)
- `docs/`: ドキュメントの変更 (例: `docs/update-readme`)
- `refactor/`: リファクタリング (例: `refactor/whisper-service`)
- `test/`: テストの追加・修正 (例: `test/add-unit-tests`)
- `chore/`: ビルド設定やツールの更新など (例: `chore/update-dependencies`)

### コミットメッセージ

コミットメッセージは明確かつ簡潔に記述してください。可能であれば [Conventional Commits](https://www.conventionalcommits.org/ja/v1.0.0/) に従うことを推奨します。

## 環境構築 (Setup)

### Lefthook (Git Hooks) の設定

本プロジェクトでは、コミット前にコードの品質確認を自動化するために [Lefthook](https://github.com/evilmartians/lefthook) を使用しています。
初回セットアップ時に以下のコマンドを実行して、Git Hooks を有効化してください。

```bash
# Lefthook がインストールされていない場合はインストール (Homebrew の場合)
brew install lefthook

# Git Hooks のインストール
lefthook install
```
