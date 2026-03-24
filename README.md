# cc-secretary

個人ファンド運営のための管理リポジトリ。

Claude Code の秘書プラグイン（`/secretary`）を中核に、日々のタスク管理・市場リサーチ・トレード記録・アイデア整理などをMarkdownベースで一元管理する。

## リポジトリ構成

```
cc-secretary/
├── .secretary/                       ← 秘書の管理データ（本体）
│   ├── CLAUDE.md                     ← 秘書の設定・ルール
│   ├── inbox/                        ← クイックキャプチャ
│   ├── todos/                        ← デイリータスク
│   ├── ideas/                        ← アイデア記録
│   ├── research/                     ← 市場分析・銘柄調査
│   ├── knowledge/                    ← ナレッジベース
│   ├── finances/                     ← トレード収支・財務
│   ├── projects/                     ← プロジェクト管理
│   ├── journal/                      ← 日記・トレード心理記録
│   └── reviews/                      ← 週次・月次レビュー
├── plugins/
│   └── secretary/                    ← Claude Code プラグイン定義
│       ├── .claude-plugin/
│       │   └── plugin.json
│       └── skills/
│           └── secretary/
│               ├── SKILL.md
│               └── references/
├── .claude-plugin/
│   └── marketplace.json
├── README.md
└── LICENSE
```

## 秘書（Secretary）

`/secretary` で起動する Claude Code プラグイン。初回はオンボーディングで対話的にセットアップし、以降は管理モードで日常操作を行う。

### コマンド一覧

| コマンド | 動作 |
|---------|------|
| タスク追加 [内容] | 今日のTODOにタスク追加 |
| 今日のタスク | 今日のタスクを表示 |
| メモ [内容] | inboxにクイックキャプチャ |
| アイデア [タイトル] | アイデアファイルを新規作成 |
| 調査 [タイトル] | リサーチファイルを新規作成 |
| 週次レビュー | 週次レビューを自動生成 |
| ダッシュボード | 全体概要を表示 |
| 受信箱整理 | inboxの整理を支援 |
| カテゴリ追加 [名前] | 新しいカテゴリを追加 |
| セットアップ確認 | 現在の秘書設定を一覧表示 |

### 管理カテゴリ

| カテゴリ | 用途 |
|---------|------|
| todos | デイリータスク管理 |
| ideas | アイデアの記録 |
| research | 市場分析・銘柄調査 |
| knowledge | ナレッジベース |
| finances | トレード収支・財務管理 |
| projects | プロジェクト管理（ファンド設立等） |
| journal | 日記・トレード心理記録 |
| inbox | クイックキャプチャ（常に含む） |
| reviews | 週次・月次レビュー（常に含む） |

## インストール

```
/plugin marketplace add Shin-sibainu/cc-secretary
/plugin install secretary@cc-secretary
```

## ライセンス

MIT
