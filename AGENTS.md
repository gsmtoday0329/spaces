# Blog Agent Guidelines

This repository is a static personal blog. It is not a slide deck, landing page, or template gallery. When creating or editing blog pages, keep the site quiet, readable, and consistent with the current design.

## Site Direction

- The blog is titled `武清南路`.
- The homepage should feel like a personal blog index, not a product pitch.
- The main subject is AI Agent evaluation experience and engineering practice. Secondary subjects can include AI-assisted learning notes about chips, macro topics, fitness, and podcast creation.
- Avoid explaining the purpose of the website too much. One concise intro on the homepage is enough.

## Visual Rules

- Use `assets/css/site.css` as the shared design system.
- Do not copy styles from `/Users/gaoshimeng/Documents/90_Archive/beautiful-html-templates-main 2` into blog posts.
- Do not make article pages look like PPT slides, one-page reports, or landing pages.
- Avoid large hero panels, decorative side cards, sticky presentation-style tables of contents, multi-column card-heavy layouts, and English label-heavy chrome.
- Article pages should be plain long-form reading pages: title, date/meta, short lead, body sections, lists, tables if useful, and a small number of callouts.
- Keep article titles smaller than homepage title scale. Blog post titles should be readable, not poster-like.
- Cards are acceptable for homepage sidebar blocks and repeated list items, but avoid nesting cards inside cards.

## Article Page Pattern

Use this structure for new regular posts:

```html
<!doctype html>
<html lang="zh-CN">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>文章标题 - 武清南路</title>
    <meta name="description" content="一句话说明这篇文章解决什么问题。" />
    <link rel="stylesheet" href="../assets/css/site.css" />
  </head>
  <body>
    <header class="site-header">
      <a class="site-title" href="../index.html">武清南路</a>
      <p class="site-description">AI Agent 评测经验和工程实践，也记录一些个人学习笔记。</p>
      <nav class="site-nav" aria-label="主导航">
        <a href="../index.html">Home</a>
        <a href="../index.html#articles">Articles</a>
      </nav>
    </header>

    <main class="post-shell">
      <article class="post">
        <header class="post-header">
          <a class="home-link" href="../index.html">返回首页</a>
          <p class="post-meta">
            <time datetime="YYYY-MM-DD">Month DD, YYYY</time>
            <span>分类</span>
            <span>标签</span>
          </p>
          <h1>文章标题</h1>
          <p class="lead">用一两句话交代文章的核心判断。</p>
        </header>

        <p>正文第一段。</p>

        <section>
          <h2>小标题</h2>
          <p>正文。</p>
        </section>
      </article>
    </main>
  </body>
</html>
```

For posts in nested folders, adjust the CSS and homepage links with the correct relative path.

## Writing Rules

- Write like a person keeping a public work note, not like a generic AI report.
- Prefer direct claims and concrete questions over abstract phrases.
- Avoid leaking company or internal project information. Public posts must not include employer names, internal project names, internal codenames, company-specific people, teams, systems, documents, URLs, screenshots, metrics, or process details.
- Avoid phrases such as `价值链路`, `闭环入口`, `强信号`, `体系化赋能`, `抓手`, `底层逻辑`, `打造`, `沉淀方法论` unless the surrounding text genuinely needs them.
- Do not overuse English labels such as `Core question`, `Strong signal`, `Decision`, `Repair`, `Evidence`.
- Avoid revealing private context. For public posts, do not frame content as job searching or interviewing unless explicitly intended.
- When discussing roles, use public framing such as `评价一个 AI Agent 评测岗位`, `判断一个团队的工作方式`, or `核对这个岗位是否能影响迭代`.
- Keep summaries specific: say what the article helps the reader decide or understand.

## Homepage Rules

- Keep the homepage intro short.
- Do not add extra philosophy blocks that explain what the site is for.
- `重点推荐` is for curated entry points, not recent posts.
- `Latest notes` is the chronological article list.
- If adding a new article, update the homepage article list and, only if it is genuinely representative, update `重点推荐`.
- Top navigation should stay compact. Do not add categories with no published articles unless the user asks.

## Verification

After editing pages:

- Start or reuse a local static server with `python3 -m http.server 8000`.
- Check changed pages with `curl -I`.
- Use Playwright screenshots for at least one desktop and one mobile viewport when layout changes are non-trivial.
- Confirm there is no obvious overflow, poster-like title scale, duplicated homepage messaging, or template attribution text.

## Publishing

Use `BLOG_PUBLISHING_SOP.md` for publishing and GitHub Pages workflow details. This file only defines writing, layout, and design conventions.
