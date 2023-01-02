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