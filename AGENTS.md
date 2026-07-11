# AGENTS.md — Column E Website

Static landing page for columne.com. **This repository is PUBLIC** — nothing
sensitive, internal, or personal goes in this repo (including in this file,
commit messages, or comments).

## Rules

- Pure static site: `index.html` + images. No build step, no framework, no JS
  dependencies — keep it that way unless explicitly asked.
- Hosted on GitHub Pages with a custom domain. The `CNAME` file is load-bearing —
  never delete, rename, or overwrite it (DNS is managed in Cloudflare; HTTPS
  enforced).
- Trunk is `master`; changes deploy automatically on push — treat every push as a
  production deploy and verify the rendered page after.
- Keep edits minimal and visual changes browser-verified before calling them done.
