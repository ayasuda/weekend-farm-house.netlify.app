# 小さな農園付き分譲地、あなたの週末セカンドハウス

> 都内で暮らしながら、週末だけ土に触れる。

構想段階のコンセプトサイトです。実在する分譲地の販売広告ではありません。

## 概要

都内在住の家族を対象にした「週末型セカンドハウス」の企画をWebサイトとして公開し、
需要・反応・共感を観測するためのコンセプトサイトです。

また、この企画を実現できる不動産会社・デベロッパー・地域事業者・自治体関係者に向けた
ゆるい企画提案でもあります。

## 技術スタック

- [Astro](https://astro.build/) v5
- TypeScript
- Netlify（ホスティング・フォーム）

## セットアップ

### 必要なもの

- Node.js 20以上

### インストール

```bash
npm install
```

## 開発コマンド

| コマンド | 説明 |
|---|---|
| `npm run dev` | 開発サーバーを起動（`http://localhost:4321`） |
| `npm run build` | 本番用ビルド（`dist/` ディレクトリに出力） |
| `npm run preview` | ビルド済みサイトをローカルでプレビュー |
| `npm run check` | TypeScript + Astroの型チェック |

## Netlifyデプロイ手順

### 1. GitHubリポジトリと接続する場合

1. Netlifyにログイン
2. 「Add new site」→「Import an existing project」を選択
3. GitHubリポジトリを選択
4. ビルド設定を確認（`netlify.toml` で自動設定されます）
   - Build command: `npm run build`
   - Publish directory: `dist`
5. 「Deploy site」をクリック

### 2. Netlify CLIを使う場合

```bash
npm install -g netlify-cli
netlify login
netlify deploy --build          # プレビューデプロイ
netlify deploy --build --prod   # 本番デプロイ
```

### Netlify Formsについて

問い合わせフォームはNetlify Formsで動作します。
Netlifyにデプロイするだけで自動的に有効になります。

受信したフォームはNetlifyダッシュボードの「Forms」から確認できます。

## コンテンツの編集

各セクションのコンテンツは以下のコンポーネントに直書きされています。

| コンポーネント | 内容 |
|---|---|
| `src/components/Hero.astro` | ヒーローセクション（キャッチコピー） |
| `src/components/About.astro` | この企画について |
| `src/components/Concept.astro` | 暮らしのコンセプト（6つの提供価値） |
| `src/components/Specs.astro` | 区画・建物イメージ |
| `src/components/Services.astro` | 農業指導・管理サービス |
| `src/components/Location.astro` | 立地イメージ |
| `src/components/Pricing.astro` | 価格イメージ |
| `src/components/FAQ.astro` | FAQ（配列で管理） |
| `src/components/Contact.astro` | 問い合わせフォーム |
| `src/layouts/Layout.astro` | SEO・OGP設定 |

FAQは `src/components/FAQ.astro` 内の `faqs` 配列を編集することで追加・変更できます。

## ライセンス

このプロジェクトはコンセプトサイトとして公開しています。
