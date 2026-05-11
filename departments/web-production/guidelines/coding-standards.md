# Web制作部 コーディング規約

## HTML

- セマンティック要素を使う (`header`, `nav`, `main`, `section`, `article`, `aside`, `footer`)
- 見出しは `h1` → `h2` → `h3` の順。スキップしない
- 画像には必ず `alt`、装飾なら `alt=""`
- フォーム要素は `label` で関連付け
- `lang="ja"` を `<html>` に設定

## CSS

- **モバイルファースト**: `min-width` でメディアクエリ
- **BEM** or ユーティリティファースト (Tailwind系) を一貫して
- CSS変数でデザイントークンを定義
- `!important` は最終手段
- リセットCSSは [modern-normalize](https://github.com/sindresorhus/modern-normalize) 推奨

### カラー変数 (標準)

```css
:root {
  --color-primary: #0066FF;
  --color-primary-hover: #0052CC;
  --color-text: #1A1A1A;
  --color-text-muted: #666;
  --color-bg: #FFFFFF;
  --color-bg-subtle: #F5F5F7;
  --color-border: #E0E0E0;
  --color-danger: #E11D48;
  --color-success: #10B981;
}
```

### タイポグラフィ

```css
:root {
  --font-sans: -apple-system, BlinkMacSystemFont, "Noto Sans JP", sans-serif;
  --font-serif: "Noto Serif JP", serif;
  --font-mono: ui-monospace, "SF Mono", Menlo, monospace;
}
```

### ブレイクポイント

```css
/* Default: mobile */
@media (min-width: 640px)  { /* sm */ }
@media (min-width: 768px)  { /* md */ }
@media (min-width: 1024px) { /* lg */ }
@media (min-width: 1440px) { /* xl */ }
```

## JavaScript

- ES Modules を使う
- `defer` or `type="module"` でロード
- ポリフィルは必要最小限
- 外部依存は `package.json` で管理
- Linter: ESLint (推奨: `eslint-config-standard` or `@antfu/eslint-config`)
- Formatter: Prettier

## ファイル構成

```
src/
├── index.html
├── assets/
│   ├── css/
│   │   ├── reset.css
│   │   ├── variables.css
│   │   ├── base.css
│   │   └── components/
│   ├── js/
│   │   └── main.js
│   └── img/
└── pages/
```

## パフォーマンス

- 画像は WebP or AVIF、`loading="lazy"`、`width/height` 必須
- フォントは subset + `font-display: swap`
- Critical CSS をインライン化
- 未使用CSSを削除 (PurgeCSS等)
- Lighthouse モバイルスコア 90以上を目安

## アクセシビリティ

- フォーカス可視化 (`:focus-visible`)
- カラーコントラスト 4.5:1 以上 (WCAG AA)
- キーボードのみで全機能操作可能
- `prefers-reduced-motion` 対応
