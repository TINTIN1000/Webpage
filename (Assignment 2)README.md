# Byron Museza — Personal Profile Page

Assignment 1: semantic HTML5 profile page.
Assignment 2: responsive styling with CSS3 (Flexbox, Grid, media queries) and Tailwind utilities.

## Responsive Notes

### Breakpoints tested
I tested the page in the browser device toolbar at all three widths:

| Device  | Width    | Result                                              |
|---------|----------|-----------------------------------------------------|
| Mobile  | ~375px   | Single column, stacked footer, no horizontal scroll |
| Tablet  | ~768px   | Two-column grid, full-width rows, footer in a row   |
| Desktop | ~1280px  | 2fr / 1fr grid, larger padding and headings         |

Approach is mobile-first: base styles target phones, then `min-width: 768px` and `min-width: 1024px` media queries layer on larger layouts.

### Flexbox vs. Grid, and why
- **Flexbox (one dimension)**
  - Footer (`styles.css`): `flex-direction`, `justify-content`, `align-items`, `flex-wrap`, `gap`. It is a single row or column of items, so Flexbox fits.
  - Header (Tailwind): `flex flex-col items-center gap-4` stacks the image, title, tagline and nav.
  - Nav (`styles.css`): `flex-direction: column` on mobile (one link per line), `row` + `justify-content: center` + `flex-wrap` + `gap` from 768px.
  - Contact form fields (Tailwind): `flex flex-col gap-*`.
- **Grid (two dimensions)**
  - Skills list (`styles.css`): `repeat(auto-fit, minmax(110px, 1fr))` with `gap`, so the number of columns adapts to the available width without a media query.
  - Overall page layout of `<main>` (`styles.css`): from 768px, 2 equal columns; from 1024px, `2fr 1fr`. Sections need to be placed in rows *and* columns, so Grid fits.

### Where Tailwind is used
- **Header** (image, title, tagline) — Tailwind utilities, including responsive variants (`sm:py-10`, `sm:w-48`, `sm:text-4xl`).
- **Contact form** — Tailwind utilities, including `md:max-w-xl` and `sm:w-auto`.

### CSS / Tailwind split (intentional)
- **Tailwind**: components with lots of small visual details (header, form controls).
- **`styles.css`**: design tokens (CSS variables), base typography, box-model card styling for `main` sections, the navigation links, the Skills grid, the footer, and the hand-written media queries.
- No element is styled by both, so there is no duplicated styling.

## Files
- `index.html` — page markup (semantic HTML5 from Assignment 1, preserved)
- `styles.css` — hand-written CSS
- `1.jpeg` — portrait image
