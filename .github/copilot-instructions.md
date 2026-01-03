# Copilot / AI Agent Instructions

Purpose
- Provide concise, actionable guidance so an AI coding agent can be productive in this repository immediately.

Big picture
- This repository is a small static portfolio site built with plain HTML and static assets. The primary entry is [index.html](index.html). Additional standalone pages live in the `public/` folder (for example [public/about.html](public/about.html)). Static images and other media live under `assets/images/`.

Project layout (key files)
- [index.html](index.html) — main landing page.
- [solution.html](solution.html) — alternate page (example content).
- [public/](public/) — additional standalone HTML pages: `about.html`, `contact.html`, `movie-ranking.html`, `birthday-invite.html`.
- [assets/images/](assets/images/) — image assets used by pages.
- [README.md](README.md) — minimal repo description.

What to edit and why
- Edit the HTML files directly. There is no build step: changes are reflected by opening the files in a browser or serving the folder.
- Keep relative paths intact when moving or renaming files; pages reference assets with relative URLs (e.g., `assets/images/...`).

Developer workflows (how to run/preview)
- Quick preview: open `index.html` in a browser from the filesystem.
- Local static server (recommended to preserve relative routing):
  - Python 3: `python3 -m http.server 8000` then open `http://localhost:8000`
  - Node: `npx serve .` if `serve` is available.
- VS Code: using the Live Server extension works fine.

Conventions & patterns found
- No JS frameworks, no package.json, no build/test tooling — treat this as static site maintenance.
- Pages in `public/` are standalone; avoid duplicating content edits — update both root and public copies where appropriate.
- Image assets are centralized in `assets/images/`; prefer reusing existing images rather than duplicating files.

Integration points & external deps
- There are no external build or runtime dependencies tracked in the repo. If asked to add tooling (bundlers, linters), document the change and add appropriate manifests.

What the agent should not assume
- There is no server-side code. Do not introduce server-specific changes without adding a lightweight local dev server and documenting it.

Examples of tasks an agent can perform immediately
- Fix typos or update copy in [index.html](index.html) and mirror changes to `public/about.html`.
- Optimize image file sizes in `assets/images/` and update `src` attributes accordingly.
- Add a small CSS file and reference it from all pages; update links consistently.

If something is unclear
- Ask the repo owner which pages are canonical when content is duplicated between root and `public/` before making wide edits.

Please review these instructions and tell me if you'd like me to add more examples, CI steps, or a local dev script.
