# NIKKEI Daily Intelligence Company

日経新聞・関連40媒体を毎日読み込み、「あなたの仕事・家計・生活・未来にどう関係するのか」が分かるレポートを発行する仮想組織です。

## 特徴

- **対象読者:** 経済の専門家ではない、一般の社会人(会社員・経営者・主婦・学生)
- **発行頻度:** 毎日(セッション起動時)
- **カバー範囲:** 日本経済新聞・Nikkei Asia・Financial Times を含む40媒体(段階的拡張中)
- **構造:** 新聞CEO + 統括補佐8AI + サイト別担当38AI

## 最新レポート

`reports/` 配下に日付別に保存:
- `reports/2026-05-28.md` ← 初版

## 起動方法

このフォルダで Claude Code セッションを開き、新聞CEOに調査を指示してください。例:

> 「本日のNIKKEI Daily Intelligence Reportを作成してください」

新聞CEOが各サイト担当AIに調査指示を出し、統括補佐AIが加工、最終レポートを `reports/YYYY-MM-DD.md` として発行します。

## 詳細

- [CHARTER.md](./CHARTER.md) — 運営マニュアル全文
- 38サイトの担当範囲は `agents/<site>/PROMPT.md` 参照
