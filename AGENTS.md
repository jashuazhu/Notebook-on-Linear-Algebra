# AGENTS

## Purpose
- Preserve concise reference chapters for vectors, matrices, spectra, and calculus in a calm, book-style presentation.
- Maintain consistent MathJax rendering so notation remains readable across chapters.

## Page Map
- public/index.html -> Table of contents for all chapters (1-10).
- public/page1basics.html -> Chapter 1: Vector Foundations.
- public/page2basics.html -> Chapter 2: Matrix Fundamentals.
- public/page3 Matrix.html -> Chapter 3: Prime Matrix Operations.
- public/page4Eigenvalue.html -> Chapter 4: Spectral Insights.
- public/page5Calculus.html -> Chapter 5: Matrix Calculus.
- Chapters 6-10 -> Reserved placeholders; future files should follow the naming pattern `page6*.html` etc. Update index and navigation once content exists.

## Layout Principles
- Shared stylesheet lives at public/styles.css; all pages should link to it and avoid inline layout CSS.
- Reading column width capped near 760px and centered with generous white space.
- Body text uses serif stack (`Georgia`, `Times New Roman` fallback); headings use Palatino-based stack; navigation uses humanist sans-serif.
- Light paper-tone background (`#f7f3e9`) with subtle card shadows for sections.
- Navigation must include previous/next links plus a `Back to Index` anchor rendered through `.chapter-nav` (disabled span when edge chapters).
- Keep typography legible on mobile: responsive padding, single-column grids, no fixed pixel font sizes under 14px.

## Design and Accessibility Guidelines
- Math formulas rely on MathJax 3 (tex-mml-chtml build) and use `$...$` or `\[ ... \]`; do not inline raw HTML entities for math.
- Use semantic headings (`h1` per page, `h2` for sections) to keep screen-reader outline sensible.
- Ensure link text remains descriptive (`Back to Index`, `Next Chapter` etc.); avoid bare "click here".
- When adding images or figures, supply `<figcaption>` descriptions and `alt` text.
- Keep color contrast above WCAG AA; prefer accent colors already defined in CSS variables.

## Editing and Extension Instructions
- When creating new chapters, start from the existing chapter template: include the header block, navigation, and wrap content inside `<article>`.
- Update `public/index.html` (table of contents) and add navigation hooks on adjacent chapters whenever a new chapter file ships.
- After substantive edits, refresh AGENTS.md, WORKLOG.md, and README.md to reflect the newest structure and decisions.
- Retain legacy copies inside `/bak` only as references; do not serve them.
- Validate HTML5 structure (e.g., with browser devtools or `npx html-validator`) before publishing changes.
