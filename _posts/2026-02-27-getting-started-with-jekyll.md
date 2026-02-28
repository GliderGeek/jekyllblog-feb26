---
title: Getting Started with Jekyll
date: 2026-02-27 00:00:00 Z
tags:
- jekyll
- tutorial
- github-pages
layout: post
author: Your Name
description: A quick primer on Jekyll — what it is, how it works, and why it pairs
  perfectly with GitHub Pages.
---

[Jekyll](https://jekyllrb.com) is a static site generator written in Ruby. You write your content in **Markdown**, define layouts in **HTML + Liquid**, and Jekyll compiles everything into a folder of plain HTML files ready to be served by any web host.

## Why Jekyll?

- **No database** — everything is a file, which means version control with git works perfectly
- **Fast** — static HTML is served directly, no server-side rendering per request
- **GitHub Pages support** — GitHub Pages has native Jekyll support, so pushing to your repo automatically rebuilds the site
- **Great for blogging** — posts are just Markdown files named `YYYY-MM-DD-title.md`

## Directory structure

A typical Jekyll blog looks like this:

```
.
├── _config.yml       # Site configuration
├── _layouts/         # HTML templates
├── _includes/        # Reusable HTML snippets
├── _posts/           # Blog posts (Markdown)
├── assets/
│   └── css/          # Stylesheets
├── index.md          # Home page
└── about.md          # About page
```

## Writing a post

Create a file in `_posts/` named `YYYY-MM-DD-my-post-title.md` with front matter at the top:

```yaml
---
layout: post
title: "My Post Title"
date: 2026-02-27
tags:
  - example
---

Your content here, written in **Markdown**.
```

Jekyll picks up the date from the filename and makes the post available at the permalink you configured.

## Front matter

The block between `---` delimiters at the top of a file is called **front matter**. It's written in YAML and lets you set variables Jekyll (and Siteleaf) will use:

| Key | Description |
|---|---|
| `layout` | Which layout template to use |
| `title` | Post or page title |
| `date` | Publication date |
| `author` | Author name |
| `tags` | List of tags |
| `description` | Short summary (used in SEO) |

## Building locally

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000` in your browser. Jekyll will watch for changes and rebuild automatically.
