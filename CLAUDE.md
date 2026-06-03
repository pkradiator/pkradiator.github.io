# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this site is

A personal blog by Priyanshu Kalal — covering personal shenanigans and deep-dives into Mathematics, Computer Science, Physics, and Electronics. Writing is the primary purpose; the tech stack should stay out of the way.

## Stack

Hugo (extended, v0.148.0+) static site with a custom theme. No Node.js, no external theme dependencies. Deployed automatically to GitHub Pages on push to `main`.

## Essential commands

```bash
hugo server -D          # local dev server (includes drafts), live-reloads at http://localhost:1313
hugo new posts/slug.md  # create a new draft post from archetype
hugo --gc --minify      # production build → public/
```

## Writing a post

New posts land in `content/posts/`. The archetype at `archetypes/default.md` pre-fills `date`, `title`, and `draft: true`. Flip `draft: false` (or remove it) when ready to publish.

For LaTeX math, wrap inline math in `$...$` and display math in `$$...$$` — MathJax is loaded automatically on pages that contain math (see `layouts/partials/extend_head.html`).

Custom shortcode available: `{{< terminal-prompt >}}` — renders an animated terminal prompt (used on the homepage).

## Configuration

Main config: `hugo.yaml`. Key sections:

- `params.math: true` — enables MathJax globally
- `menu.main` — controls top-nav items (Categories, Tags, Archives, Search)
- Search uses Fuse.js; tuning weights live in `hugo.yaml` under `outputs` and `fuseOpts`

## Deployment

Push to `main` → GitHub Actions (`.github/workflows/hugo.yaml`) builds and deploys to GitHub Pages automatically. No manual step needed.
