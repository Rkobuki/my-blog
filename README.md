# my-blog
kobuki`s blog

## 記事の投稿方法

1. `content/posts/`ディレクトリに新しいMarkdownファイルを作成
2. ファイル名は「YYYY-MM-DD-title.md」形式で作成
3. ファイルの先頭にFront Matterを記述
4. 記事本文をMarkdown形式で記述

## ファイル命名規則

- 例: `2025-03-07-new-post.md`
- 日付は投稿日をYYYY-MM-DD形式で記述
- タイトルはハイフン区切りの英数字で記述

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

## Markdown記法の基本

- 見出し: `#`, `##`, `###`
- リスト: `- ` または `1. `
- リンク: `[text](url)`
- 画像: `![alt](url)`
- コードブロック: ``` ``` ```
- 強調: `**太字**`, `*斜体*`
