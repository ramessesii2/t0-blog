# Tzero Blog

The repository that powers the Tzero community blog static site. Built with Hugo and the pehtheme-hugo theme. If you can open a pull request, you can publish a post.

## Quick start

1. Create a new post:

   ```bash
   hugo new posts/YYYY/YYYY-MM-DD__title-of-your-post.md
   ```

2. Open the generated file and fill in front matter (see below).

3. Add any images into `assets/images/`.

4. Preview locally:

   ```bash
   npm install
   npm run dev
   ```

5. When ready to publish, set `draft: false` and open a pull request.

## Front matter (copy–paste)

```yaml
---
title: "Your Post Title"
date: 2025-01-15
author: "Your Name"
tags: ["automation", "kubernetes", "devops"]
draft: true
description: "A brief description of your post"
image: "images/your-image.jpg"
---
```

Write Markdown content **below** the front matter.

Additional notes:

- `date` is YYYY-MM-DD format.
- Leave `draft: true` while iterating; change to `false` to publish.
- `tags`, `categories`, and `image` are optional.

## Images & media

- Place images in `assets/images/`.

- Reference them in front matter:

  ```yaml
  image: "images/your-image.jpg"
  ```

- Aim for small files (<1 MB). Add meaningful alt text.

## Local development

Prerequisites:

- Git (for cloning the repository and its submodule)
- Hugo (standard version, not extended)
- Node.js (v16+) and npm

```bash
git clone https://github.com/mirantis/t0-blog.git
cd t0-blog
git submodule update --init --recursive
npm install
```

Start a live-reloading development server:

```bash
npm run dev
```

Visit http://localhost:1313/ to preview the site.

For Hugo-only mode (faster, no CSS changes):

```bash
hugo server -D
```

## Pull request checklist

- `title`, `date`, `author`, `description` set
- `draft: false` for publishing
- Images load
- Links/code blocks render correctly
- Post matches the tone and headings of existing posts

## Conventions

- **File name**: use format `YYYY-MM-DD__kebab-case-title.md`
- **Code blocks**: use fenced blocks with language hints (e.g., `sh`, `yaml`)
- **Internal links**: prefer relative links within the repository

## License

See [LICENSE](LICENSE) file for details.
