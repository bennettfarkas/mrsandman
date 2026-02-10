# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

mrsandman.ai — personal site for Bennett Farkas. Static HTML hosted on GitHub Pages with Cloudflare DNS.

## Deploy

Push to `main`. GitHub Pages deploys automatically. The `CNAME` file maps the custom domain — don't delete it.

## Architecture

Pure static site. No build step, no bundler, no framework. Inline CSS in `index.html`. Open the file in a browser to preview locally.

## Tone

Quick, smart, witty, candid. Copy should feel conversational, not corporate.

## Design

- Dark theme (`#0a0a0a` background)
- Display: Bricolage Grotesque (800) — headlines
- Body: Plus Jakarta Sans (400/500/600) — text, buttons, inputs
- Mono: JetBrains Mono (400) — status pills, technical accents only
- Accent gradient: `#c9a0ff` (purple) to `#7eb8ff` (blue)
- Body weight 500 (Medium) as default — 400 looks thin on dark backgrounds
