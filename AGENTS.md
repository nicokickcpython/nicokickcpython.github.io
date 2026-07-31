# AGENTS.md

这是 `nicokickcpython/nicokickcpython.github.io` 技术博客仓库的 agent 友好说明。

## 这是什么仓库

个人技术博客（GitHub Pages + Jekyll）。文章用 Markdown 编写，Jekyll 构建为静态站点。

## 内容在哪

- 所有文章位于 `_posts/` 目录，命名遵循 Jekyll 约定：`YYYY-MM-DD-slug.md`
  - 例如 `_posts/2026-07-31-autopublish-f99c.md`
- `index.md` 是文章列表首页

## 机器可读入口

- `feed.xml` — RSS 2.0 + Atom 混合，用 `site.posts` liquid 循环生成
- `posts.json` — 结构化文章索引，包含每篇文章的 title / slug / url / date / tags / raw

## 如何获取原文

每篇文章的原文 raw URL 规则：

```
https://raw.githubusercontent.com/nicokickcpython/nicokickcpython.github.io/main/_posts/YYYY-MM-DD-slug.md
```

即从 `posts.json` 中的 `raw` 字段直接抓取 Markdown 原文。

## Frontmatter 字段说明

每篇文章的 frontmatter 支持以下字段：

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| `title` | string | 文章标题（必填） |
| `date` | string | 发布日期，格式 `YYYY-MM-DD`（Jekyll 自动从文件名读取，可覆盖） |
| `layout` | string | 布局，默认 `post` |
| `tags` | array | 文章标签，例如 `["python"]` |
| `description` | string | 文章摘要，用于列表页和 feed |
| `permalink` | string | 可选，自定义 URL |

## 约定

- 不要修改已发布文章的 frontmatter 之外的正文
- 不要引入外部依赖（无 CDN、无 Google Fonts、无 JS 库）
- 界面为中文
