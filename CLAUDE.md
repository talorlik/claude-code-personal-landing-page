# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A static personal landing page, built as a course assignment. No build step,
no package manager, no framework. Everything served directly from `docs/` via
GitHub Pages.

Live URL: [https://talorlik.github.io/claude-code-personal-landing-page/](https://talorlik.github.io/claude-code-personal-landing-page/)

## Development

Open `docs/index.html` in a browser directly, or serve it locally:

```bash
python3 -m http.server 8080 --directory docs
```

Then open [http://localhost:8080](http://localhost:8080).

There is no linter, formatter, or test suite configured.

## Structure

```bash
docs/
  index.html          # Single-page site - all content lives here
  styles.css          # All styling; uses CSS custom properties defined in :root
  main.js             # Injects JSON-LD structured data (Schema.org) on DOMContentLoaded
  favicon.ico
  header_banner.png   # Hero image (AI-generated)
  profile-pic.jpg     # Profile photo (AI-generated)
  profile-icons/      # SVG icons not available from CDNs (cursor.svg, openai.svg)
  generated/          # GitHub stats SVGs (stats.svg, top-langs.svg, streak.svg)
```

## Key Design Decisions

**CSS custom properties** - all colors, spacing, and breakpoints are defined as
variables in `:root` in `styles.css`. Change the palette there, not inline.

**No external JS dependencies** - `main.js` is vanilla JS wrapped in an IIFE.
Keep it that way.

**Icon sources** - tech stack icons come from two CDNs:

- `https://skillicons.dev/icons?i=<name>&perline=1` for most icons
- `https://cdn.simpleicons.org/<name>/<hex-color>` for icons not in skillicons
- `./profile-icons/<name>.svg` for icons not available on either CDN

**GitHub stats SVGs** - the three files in `docs/generated/` are static snapshots.
They are not auto-refreshed in this repo (unlike the source repo, which uses
GitHub Actions to regenerate them).

**`main.js` canonical base** - the `CANONICAL_BASE` constant points to the
original `talorlik.github.io/talorlik` URL. Update it if SEO metadata needs to
reflect this repo's URL instead.
