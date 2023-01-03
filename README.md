# Outline

voltaでnodeバージョンを管理している  
環境にないのなら以下を参考に導入
https://docs.volta.sh/guide/getting-started

```agsl
npm run dev
```

で localhost:3000 にアクセスできる


# Todo
  
- [x] Next.jsの雛形作成
- [x] volta導入
- [x] prettier導入
- [ ] Markdown形式 (プラグイン or MDX or Contentlayer)
- [ ] Storybook対応
- [ ] CSSフレームワーク対応
- [ ] Jest対応
- [ ] テスト追加
- [ ] CircleCI導入
- [ ] Github Pagesデプロイ
- [ ] SEO (next-seo?)

# 開発ログ

## Step1  

```agsl
npx create-next-app@latest pre-blog
```

で雛形作成  
  
READMEのTodo作成

## Step2

voltaでnodeのバージョンを管理するようにする

```agsl
volta pin node@18.12.1
```

Outline、Todo追記

## Step3

Prettierの追加

```agsl
npm install -s -D prettier eslint-config-prettier
```

.eslintrc.jsonの変更  

## Step4

Markdown形式ブログにするにあたってMDXかContentlayerのどちらにするか検討 → 公式サポートなどを鑑みて今回は一旦MDXを試すことにする

```agsl
npm install -s @next/mdx @mdx-js/loader @mdx-js/react
```

next.config.jsに以下を追記
```agsl
const withMDX = require('@next/mdx')({
  extension: /\.mdx?$/,
  options: {
    // If you use remark-gfm, you'll need to use next.config.mjs
    // as the package is ESM only
    // https://github.com/remarkjs/remark-gfm#install
    remarkPlugins: [],
    rehypePlugins: [],
    // If you use `MDXProvider`, uncomment the following line.
    // providerImportSource: "@mdx-js/react",
  },
})
module.exports = withMDX({
  // Append the default value with md extensions
  pageExtensions: ['ts', 'tsx', 'js', 'jsx', 'md', 'mdx'],
})
```

サンプルとしてpages/my-mdx-page.mdxを用意  
  
Todo追記