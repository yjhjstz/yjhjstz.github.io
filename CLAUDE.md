# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Jekyll 4.4+ static site — a personal technical blog hosted on GitHub Pages at yjhjstz.github.io. Custom dark developer theme (no external theme gem). Content is primarily database internals (LevelDB, PostgreSQL, MongoDB).

## Build & Development Commands

```bash
# Install dependencies
bundle install

# Local development server (http://localhost:4000)
bundle exec jekyll serve

# Production build (output to _site/)
bundle exec jekyll build
```

## Architecture

- **`_config.yml`** — Site config: kramdown+GFM markdown, rouge highlighter, jekyll-paginate (20/page), jekyll-seo-tag. Permalink: `/:title/`.
- **`_layouts/`** — Three templates: `default.html` (shell with nav/footer), `post.html` (extends default, adds reading progress bar + prev/next nav), `page.html` (extends default).
- **`_includes/`** — Analytics snippets (Google, Baidu) and social sharing (JiaThis). Included from `default.html`.
- **`media/css/style.css`** — All styling in one file using CSS custom properties. Dark theme (`#0d1117` bg, `#00e676` accent). Mobile breakpoint at 640px.
- **`_posts/`** — Markdown posts with YAML front matter (`layout`, `title`, `date`, `categories`, `tags`).
- **`index.html`** — Homepage with hero section, tag cloud, and paginated post list.
- **Static pages** — `about/`, `categories/`, `tags/`, `github/`, `guestbook/` each with their own `index.md`.

## Content Conventions

- Posts use `layout: post` in front matter
- Pages use `layout: page` in front matter
- Static assets (images for posts) go in `assets/` subdirectories
- CSS and JS live under `media/css/` and `media/js/`
