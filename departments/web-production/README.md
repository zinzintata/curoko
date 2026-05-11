# Web制作部 作業フォルダ

## サブフォルダ

- `projects/` — プロジェクトごとの作業フォルダ (1案件1フォルダ)
- `templates/` — 要件定義書など再利用可能なテンプレ
- `guidelines/` — コーディング規約など社内ルール

## プロジェクト開始手順 (web-director が実行)

1. `projects/<project-name>/` を作成
2. `templates/project-brief-template.md` を `projects/<project-name>/brief.md` にコピー
3. ユーザー(クライアント)から要件をヒアリングして brief.md を埋める
4. 以降のフェーズで配下の専門部門を適切に呼び出す

## サブ部門エージェント

| エージェント | 役割 |
|---|---|
| `web-director` | プロジェクトマネジメント (このフォルダのエントリーポイント) |
| `web-planner` | 企画・IA・サイトマップ・ワイヤー |
| `web-designer` | UI/UX・ビジュアル |
| `web-copywriter` | Webコピー・マイクロコピー |
| `web-frontend` | HTML/CSS/JS実装 |
| `web-backend` | API/DB/サーバー |
| `web-seo` | SEO・パフォーマンス |
| `web-qa` | QA・アクセシビリティ |
