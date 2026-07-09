# Editorial magazine template — horizontal drag gallery

**Live demo → https://bswxyz.github.io/formwork-atelier/** · [How it was built](https://bswxyz.github.io/formwork-atelier/guide/)

> A cream, image-free fashion editorial with a momentum drag-scroll gallery of typographic plates.

A free, MIT-licensed website template. Good for: **magazines, lookbooks, editorial portfolios, photography (drop images into the plates)**.
The demo brand ("ATELIER NOIR") is fictional — every word and colour is meant to be replaced with yours.

## The signature technique

- Pointer drag-scroll with inertia; mouse wheel converts to horizontal inside the gallery
- Per-plate parallax between duotone ground and serif title
- Custom 'DRAG' cursor; degrades to native snap-scroll on touch

## Use this as your own site

This repo is a **template** — everything is plain HTML/CSS/JS with **relative paths**, so it
works under *any* repo name with zero configuration.

1. Click **Use this template → Create a new repository** (top of this page).
   **Name it whatever you like** — `my-site`, `portfolio`, anything.
2. In your new repo: **Settings → Pages → Build and deployment → Deploy from a branch**,
   then pick `main` / `/ (root)` and save. (CLI: see below.)
3. Wait ~1 minute. Your site is live at `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`.

<details>
<summary>Prefer the command line?</summary>

```bash
gh repo create my-site --template bswxyz/formwork-atelier --public --clone
cd my-site
gh api --method POST /repos/YOUR-USERNAME/my-site/pages \
  -f 'source[branch]=main' -f 'source[path]=/'
```
</details>

No build step, no dependencies to install — edit the files, push, done.
The only external requests are Google Fonts and (where used) pinned CDN copies of GSAP/three.js.

## Customize it

- Plates: each look is one `<article>` — set its duotone gradient vars and titles in `index.html`
- Masthead/issue: cover lines and `N°` live at the top of `index.html`
- Palette: cream/ink/oxblood in `:root` — swap for your editorial colours

The `/guide/` page documents the signature technique in depth (with code) — keep it, rewrite it,
or delete the folder entirely.

## Files

```
index.html        the page
styles.css        all styling (design tokens in :root at the top)
main.js           the signature effect + motion
guide/index.html  how-it-works write-up (optional — yours to keep or delete)
```

## Built-in quality

- Works with JS disabled or a CDN failure (content is never permanently hidden)
- Respects `prefers-reduced-motion`; keyboard focus styles throughout
- Canvas/WebGL feature-detected with graceful fallbacks; devicePixelRatio capped for performance
- Responsive at phone / tablet / desktop widths

## License & credit

[MIT](LICENSE) — free for personal and commercial use, no attribution required
(a link back is always appreciated). Part of **FORMWORK** — a collection of
25 free website templates: **[the full gallery →](https://bswxyz.github.io/formwork/)**
