# 小さな農園付き分譲地、あなたの週末セカンドハウス

都内在住の家族に向けた、週末型セカンドハウス構想のコンセプトサイトです。実在する分譲地の販売広告ではなく、需要・反応・共感を観測するための静的Webサイトです。

## 技術構成

- Astro
- TypeScript
- Netlify Forms
- 静的サイト出力

## セットアップ

```bash
npm install
```

## 開発コマンド

```bash
npm run dev
```

ローカル開発サーバーが起動します。通常は `http://localhost:4321` で確認できます。

```bash
npm run build
```

型チェックと本番ビルドを実行します。出力先は `dist/` です。

```bash
npm run preview
```

ビルド済みサイトをローカルでプレビューします。

## Netlifyへのデプロイ

1. このリポジトリをGitHubへpushします。
2. Netlifyで「Add new site」からGitHubリポジトリを選択します。
3. Build command に `npm run build` を設定します。
4. Publish directory に `dist` を設定します。
5. Deployします。

`netlify.toml` に同じ設定を含めているため、Netlify側で自動検出されます。

## 問い合わせフォーム

トップページ内の「興味・感想フォーム」は Netlify Forms に対応しています。

- form name: `interest`
- method: `POST`
- `data-netlify="true"` を指定
- honeypot項目あり

Netlifyにデプロイ後、Forms画面で送信内容を確認できます。

## コンテンツ編集

企画文やFAQ、フォームの選択肢などの主要テキストは [src/data/site.ts](src/data/site.ts) にまとめています。

ページ構造とスタイルは以下です。

- [src/pages/index.astro](src/pages/index.astro)
- [src/styles/global.css](src/styles/global.css)

## 注意

このサイトは構想段階のコンセプトサイトです。価格・区画数・設備・サービス内容・法規制・建築可否はすべて仮説であり、実際の販売情報ではありません。
