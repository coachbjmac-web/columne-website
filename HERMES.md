# HERMES.md — Column E Website

> Hermes loads exactly ONE project-context file per repo: `HERMES.md` > `AGENTS.md` >
> `CLAUDE.md` > `.cursorrules`, first match wins. This repo's `AGENTS.md` still exists and
> is accurate — open it directly if you need it, it is not injected alongside this file.

**This repository is PUBLIC.** Nothing sensitive, internal, or personal goes in this repo —
not in code, not in commit messages, not in this file.

## What this is

A static marketing/landing page. Pure HTML/CSS/JS — no framework, no build step, no
dependencies. Single `index.html` in the repo root plus an `img/` directory and a couple of
root-level images.

## Stack & structure

- Entry: `index.html` — single page, inline `<style>` and `<script>`, no external JS/CSS
  dependencies.
- No `package.json`, no bundler, no compile step — edit `index.html` (and assets) directly
  and the change is the deploy artifact.

## Deploy

- Hosted on GitHub Pages (legacy build type) from the `master` branch, site root `/`.
- A custom domain is configured via a `CNAME` file in the repo root. **This file is
  load-bearing for DNS — never delete, rename, or overwrite it.**
- **Every push to `master` deploys to production immediately.** There is no staging
  environment and no test suite — treat each push as a live production deploy.
- DNS and HTTPS are managed outside this repo (external DNS provider + GitHub Pages
  settings). A broken deploy is not always fixable from inside this repo alone — say so
  rather than guessing at external config you cannot see.

## Non-negotiables

- **Never run destructive git operations** (force-push, history rewrite, branch deletion)
  without explicit authorization for that specific action.
- **NEVER GUESS** at content, copy, or structure — if you don't know what a section should
  say or look like, ask or leave it alone. Don't invent plausible-sounding text.
- **Never claim a change is "done" without verifying the live rendered page after deploy.**
  A static site has no test suite to catch a broken layout or a syntax error — a single
  unclosed tag can break the whole page silently.
- **Keep edits minimal.** No build step means no compile-time warning for a mistake; small,
  reviewable diffs are the only safety net this repo has.
