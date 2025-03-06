---
title: "Blogの立ち上げ ～Cloudflare Pages × Hugo～"
date: 2025-03-07T00:29:40+09:00
draft: false
---


## はじめに
自分が気ままに投稿できるような場がほしいと前から思っていました。そんななか、Cloudflare Pagesを使えば無料でブログを開設できると聞きました。

**無料で！** 👀

ということで、実際にやってみます。Cloudflare PagesやSSGの練習になるといいな！

<!--more-->

---

## 選んだ技術スタック
### GitHub + SSG + Cloudflare Pages
ブログを運用するために、以下の技術を使います。
- GitHub：原稿管理・バージョン管理
- SSG（Hugo）：静的サイトを生成
- Cloudflare Pages：無料でデプロイできるホスティングサービス

この組み合わせなら、サーバー代も不要で運用コストゼロだそう（by GPT-4o）。
しかも、Markdownで記事を書いてGitHubにプッシュすれば自動でデプロイされるので、手軽に管理できそう。

---

## SSG（静的サイトジェネレーター）選び
ブログを作るにあたって、どのSSGを使うか悩んだ。
候補は以下の3つ。

| SSG | 特徴 |
|----|----|
| Hugo | Go製。高速ビルド |
| Jekyll | Ruby製。GitHub Pagesとの相性◎ |
| 11ty | JavaScript製。カスタマイズ性◎ |

11tyではうまくいかず(´;ω;｀)

結局は、Hugoを選択。Hugoはかなりビルドが速く快適だった。

---

## Cloudflare Pages の魅力

実際に使ってみて、Cloudflare Pagesの良さが少し分かった。

### 1. 無料
- デプロイ回数の制限なし（月500回まで）
- 帯域幅も無制限
- 商用利用もOK なので、個人ブログだけでなく、プロジェクトサイトにも使えるそう

### 2. GitHubと連携すると簡単
- リポジトリを指定するだけで、自動デプロイができる
- Push するだけでブログが更新される のは快適

### 3. SSL対応やCDNが標準装備
- HTTPS対応が自動（手動で証明書を用意する必要なし）
- CloudflareのCDNが使える ので、ページの表示が速い

---

## 実際のセットアップ
- 1. GitHubリポジトリを作成
- 2. Hugoのインストール
```powershell
choco install hugo  # Windowsなので
```

- 3. 新しいHugoサイトを作成
```powershell
hugo new site my-blog
cd my-blog
```

- 4. テーマを追加
```sh
git init
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke themes/ananke
```

- 5. 設定ファイルを編集（`config.toml`）
```toml
theme = "ananke"
baseURL = "https://your-site.pages.dev/"
```

- 6. Cloudflare Pagesでデプロイ
1. [Cloudflare Pages](https://pages.cloudflare.com/) にアクセス
2. GitHubと連携 → `my-blog` を選択
3. Build command: `hugo --minify`
4. Publish directory: `public`
5. デプロイ開始！

---

## まとめ
とりあえずブログを開設できたので大満足。
これからは勉強したことだったり、読んだ本の話だったり、どこか行った話だったり、気軽に投稿していきたい！
