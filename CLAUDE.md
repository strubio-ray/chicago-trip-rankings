# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A curated Chicago Airbnb/VRBO trip rankings guide published as a static Jekyll site on GitHub Pages. The site ranks and compares 5 short-term rental properties across Chicago neighborhoods with detailed specs, photo galleries, and neighborhood guides.

## Architecture

- **Content**: `README.md` is the primary content document (all listing data, comparisons, neighborhood guides)
- **Jekyll entry point**: `index.md` pulls in README.md via `{% include_relative README.md %}`
- **Layout**: `_layouts/default.html` — minimal responsive template using GitHub Markdown CSS from CDN, with dark mode support
- **Config**: `_config.yml` — minimal Jekyll configuration

No backend, no JavaScript, no build tools, no dependencies to install.

## Local Development

```bash
jekyll serve
```

There are no tests, linters, or package managers configured.

## Deployment

Pushes to the main branch trigger automatic GitHub Pages builds. No manual deployment steps needed.

## Content Structure

Each listing section follows a consistent pattern: quick comparison table → "At a Glance" specs → photo gallery (embedded CDN URLs) → neighborhood guide with restaurant/bar/coffee recs → transit access → host info.
