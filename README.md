# Tzero Blog

The repository that powers the Tzero community blog static site. Built with Hugo and the pehtheme-hugo theme. **If you can open a pull request, you can publish a post.**

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Hugo** (latest version recommended)
  - Install via [Hugo's official guide](https://gohugo.io/installation/)
  - This project uses standard Hugo (not extended version)
  - Verify installation: `hugo version`

- **Node.js** (v16 or higher) and **npm**
  - Required for TailwindCSS workflow
  - Install via [Node.js official website](https://nodejs.org/)
  - Verify installation: `node --version` and `npm --version`

## 🚀 Local Development Setup

### 1. Clone the repository

```bash
git clone https://github.com/mirantis/t0-blog.git
cd t0-blog
```

### 2. Initialize theme submodule

The blog uses the pehtheme-hugo theme as a git submodule:

```bash
git submodule update --init --recursive
```

### 3. Install npm dependencies

Install TailwindCSS and related dependencies:

```bash
npm install
```

### 4. Start the development server

You have two options for running the development server:

**Option A: Hugo only (faster, no CSS changes)**
```bash
hugo server -D
```

**Option B: Hugo + TailwindCSS watch mode (for styling changes)**
```bash
npm run dev
```

## ✍️ Creating New Blog Posts

### Using Hugo's archetype command

To create a new blog post with the proper structure:

```bash
hugo new posts/YYYY/YYYY-MM-DD__title-of-your-post.md
```

For example:
```bash
hugo new posts/2025/2025-01-15__reducing-kubernetes-toil.md
```

This will create a new post file with pre-populated frontmatter in the `content/posts/YYYY/` directory.

### Post frontmatter structure

Each post should include the following frontmatter (automatically added by the archetype):

```yaml
---
title: "Your Post Title"
date: 2025-01-15
author: "Your Name"
tags: ["automation", "kubernetes", "devops"] (OPTIONAL)
categories: ["Engineering"] (OPTIONAL)
draft: true
description: "A brief description of your post"
image: "images/your-image.jpg" (OPTIONAL)
---
```

### Adding images to posts

1. Place images in the `assets/images/` directory
2. Reference them in your post frontmatter or content:
   ```yaml
   image: "images/your-image.jpg"
   ```
3. In markdown content, use:
   ```markdown
   ![Alt text](/images/your-image.jpg)
   
This will:
1. Generate optimized TailwindCSS styles
2. Build the Hugo site

The `public/` directory will contain the complete static site ready for deployment.

## 📄 License

See [LICENSE](LICENSE) file for details.

---

