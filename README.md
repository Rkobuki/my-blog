# my-blog
[kobuki's blog](https://rikuro-kobuki.com/)

## 記事の投稿方法

1. `content/posts/`ディレクトリに新しいMarkdownファイルを作成
2. ファイル名は「YYYY-MM-DD-title.md」形式で作成
3. ファイルの先頭にFront Matterを記述
4. 記事本文をMarkdown形式で記述

## ファイル命名規則

- 例: `20250307-x.md`
- 日付は投稿日をYYYY-MM-DD形式で記述

## Front Matterの記述例

```markdown
---
title: "記事のタイトル"
date: 2025-03-07
draft: false
tags:
  - tag1
  - tag2
categories:
  - category1
---
```

## 主要なファイルとディレクトリ

```
my-blog/
├── hugo.toml          # Hugoの設定ファイル
├── content/           # 記事コンテンツ
│   ├── _index.md      # トップページ
│   └── posts/         # 記事ディレクトリ
│       └── first-post.md  # サンプル記事
├── themes/            # テーマディレクトリ
│   └── ananke/        # Anankeテーマ
├── assets/            # 静的アセット（CSS/JSなど）
├── public/            # ビルド出力ディレクトリ
└── _site/             # 開発用ビルド出力
    ├── index.html     # ビルドされたトップページ
    └── posts/         # ビルドされた記事
        └── first-post/
            └── index.html
```

### 主要ファイルの説明

- **hugo.toml**: サイト全体の設定ファイル
- **content/**: 記事を管理するディレクトリ
- **themes/ananke/**: 使用しているHugoテーマ
- **assets/**: カスタムCSSやJavaScriptファイル
- **_site/**: 開発サーバー用のビルド出力
- **public/**: 本番用ビルド出力
