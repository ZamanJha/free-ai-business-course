# Free AI Business Course

Static course site — plain HTML lesson pages, no LMS, deploys to Vercel with zero config (matches the same pattern as ai-advertiser-course.vercel.app).

## Structure

```
index.html                     Course map / index — lists all modules and lessons
modules/
  module-1/
    1.1-lesson.html
    1.2-lesson.html
  module-2/
    2.1-lesson.html
    2.2-lesson.html
assets/
  css/style.css                 Shared dark-terminal design system
```

This is currently a **placeholder skeleton** — two modules, two lessons each — to prove out the pattern (navigation, video embed slot, Base44-step callout, lesson-to-lesson nav). The real module count, titles, and content still need to be designed.

## Adding a new lesson

1. Copy an existing `X.Y-lesson.html` file into the right module folder.
2. Update: `<title>`, breadcrumb, `<h1>`, description, video embed `src`, body content, and the prev/next links in `.lesson-nav`.
3. Add a row for it in `index.html`'s module list.

## Design system

All shared styling lives in `assets/css/style.css` (CSS custom properties at the top for colors/fonts). The current palette (dark background, green terminal accent) is a placeholder built from a description of the original landing page — swap the tokens once the actual landing page file is available so the two match exactly.

## Deploying

No build step. Push to GitHub, import the repo at vercel.com/new, done — Vercel serves the static files directly and auto-redeploys on every push to `main`.
