# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static website for Sunlark, a Sydney-based alt-rock/grunge band. No build system, framework, or package manager — just plain HTML and CSS served directly.

## Architecture

- `index.html` — Public landing page with streaming links, social links, and band member info
- `samples.html` — Hidden/unlisted page (`noindex, nofollow`) for sharing early rehearsal recordings with select people
- `style.css` — Single shared stylesheet using CSS custom properties (defined in `:root`)
- `images/` — Logo, favicon, cover art
- `media/` — Audio files (rehearsal recordings)

## Infrastructure

- **Domain**: sunlarkband.com via Porkbun
- **Hosting**: Netlify, auto-deploys from GitHub repo `sam-roberts/sunlark-band`
- **Analytics**: Cloudflare Web Analytics (client-side script in `index.html`)

## Development

No build step. Open HTML files directly in a browser or use any local server (e.g., `npx serve` or `python -m http.server`). Push to `main` to deploy.

## Design

- Color scheme: pink background (`#fac2c2`) with near-black text (`#050505`), defined as CSS custom properties
- Typography: Helvetica Neue / Arial / sans-serif
- Layout: Single centered column, max-width 500px
- Mobile responsive via `@media (max-width: 768px)`
