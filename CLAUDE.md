# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is Hui Zhang's personal academic website (zdchan.github.io), a static site hosted on GitHub Pages. It is forked from Jon Barron's academic website template.

## Architecture

- `index.html` — Single-page site with all content: bio, publications, invited talks, academic service. Includes inline JavaScript for smooth scrolling (dark mode toggle exists but is commented out).
- `stylesheet.css` — All styling, including fonts (Inter, Playfair Display, Lato), responsive layout, animations, and a commented-out dark mode theme.
- `images/` — Profile photo, publication demo videos (.mp4), and other media.
- `data/` — BibTeX files for publications and a CV PDF.
- `mipnerf/`, `mipnerf360/`, `zipnerf/` — Standalone project pages (each with their own `index.html`, CSS, JS, and media). These use Bootstrap and have their own self-contained structure.

## Development

No build system, bundler, or package manager. Edit HTML/CSS directly. Preview by opening `index.html` in a browser or using any local HTTP server:

```
python3 -m http.server 8000
```

Deploy by pushing to the `master` branch — GitHub Pages serves from it automatically.

## Key Patterns

- Publications are added as `<div class="publication-item">` blocks in the publications section of `index.html`, each containing a media element (video/image), metadata, and links.
- Talks are `<div class="talk-item">` blocks in the talks section.
- Academic service entries follow a similar div-based pattern under the academic service section.
- CSS classes use BEM-like naming: `.publication-item`, `.publication-media`, `.publication-content`, `.publication-title`, etc.
