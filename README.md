# Digital Book Notes

## Overview
- Lightweight static companion that walks through vector and matrix topics in a chaptered, book-style layout.
- MathJax powers inline and display notation; no build pipeline is required.
- Design goals: narrow reading width, serif body copy, calm paper background, and consistent chapter navigation.

## Folder Structure
- public/
  - index.html (table of contents for all chapters)
  - page1basics.html .. page5Calculus.html (chapters 1-5)
  - styles.css (shared book styling)
- bak/ (reference copies of the original pages)
- AGENTS.md, WORKLOG.md, README.md (project guidance and status)

## Viewing Locally
1. Open `public/index.html` in a modern browser (MathJax loads from CDN, so network access is required for formulas).
2. Use the chapter navigation within each page to move forward/back or return to the index.

## Style Summary
- Palette: paper background `#f7f3e9`, page surface `#ffffff`, ink `#1e1a17`, accent copper `#7c4b2d`.
- Typography: body uses `Georgia`-style serif; headings rely on Palatino-family serif; navigation uses `Segoe UI`/sans stack.
- Layout: main column capped near 760px with generous padding and card-style sections; responsive rules collapse navigation to stacked buttons on narrow screens.

## Editing and Deployment
- Edit chapter content inside `public/pageN*.html`; keep MathJax delimiters (`$...$`, `\[...\]`) and avoid introducing inline layout CSS.
- When adding a new chapter: duplicate an existing page, update the header metadata, adjust navigation links, and register the chapter inside `public/index.html`.
- Run HTML validation (browser devtools or external checker) after large changes; ensure MathJax still renders key formulas.
- Refresh AGENTS.md, WORKLOG.md, and this README with any new conventions or structural choices.
- Deploy by serving the `public/` directory with any static host (GitHub Pages, Netlify, local file protocol). No build step is necessary.
