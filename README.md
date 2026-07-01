# KelvSec

The source for [kelvsec.ie](https://kelvsec.ie), a cybersecurity projects and practical guidance site built with Jekyll and hosted natively on GitHub Pages.

## Publishing a blog post

Create a Markdown file in `_posts` using the filename format `YYYY-MM-DD-short-title.md`:

```yaml
---
title: Your article title
description: A concise summary used in listings and search metadata.
date: 2026-07-01 09:00:00 +0100
categories:
  - Web security
tags:
  - example
  - defensive security
---
```

Write the article below the closing `---`. GitHub Pages publishes it at `/blog/short-title/` after the commit reaches the publishing branch.

## Publishing a project

Create a Markdown file in `_projects`. Its filename becomes its URL under `/projects/`:

```yaml
---
title: Your project title
description: A concise summary of the project.
date: 2026-07-01 10:00:00 +0100
status: Complete
categories:
  - Web security
tags:
  - methodology
---
```

Project pages automatically use the project layout and appear on the Projects index.

Suggested project statuses are `In progress`, `Complete` and `Maintained`. Update the `status` value whenever the state of a project changes.

## Local preview

GitHub Pages builds the site automatically. If Ruby and Bundler are already available locally, the GitHub Pages gem can also be used to preview the site:

```bash
bundle exec jekyll serve
```

Open `http://127.0.0.1:4000`. The production custom domain is defined by `CNAME`; keep that file unchanged.

## Site structure

- `_layouts` contains reusable page, post and project layouts.
- `_includes` contains the shared header and footer.
- `_posts` contains dated blog posts.
- `_projects` contains project articles.
- `assets/css/kelvsec.css` contains the site styles.
- `assets/images` contains favicon and social-sharing assets.
- `index-backup.html` is the preserved pre-Jekyll landing page and is excluded from the generated site.
