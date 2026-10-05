# grizzeti.bg

Static replacement for the old WordPress site. No build step, no database, no plugins.

```
index.html      the page (Bulgarian)
styles.css      all styles; colours and fonts are tokens at the top
main.js         mobile menu + header shadow
assets/img/     optimised images used by the site (WebP/PNG)
assets/src/     original images downloaded from the old site (not needed for deploy)
```

## Preview locally
Open `index.html` in a browser, or run `python -m http.server` in this folder and visit http://localhost:8000.

## Editing
- **Prices / product links:** each product is an `<article class="product">` in `index.html`.
- **Sold-out product:** add `is-soldout` to the article and swap the button (see "Обикновени бисквити").
- **Colours:** change the `--pink`, `--blue`, `--yellow`, `--brown` tokens in `styles.css`.

## Deploy (free)
1. Create a free account on Netlify or Cloudflare Pages.
2. Drag this folder (without `assets/src`) into "Deploy manually", or connect a Git repo.
3. Add the custom domain `grizzeti.bg` and update DNS at your registrar as instructed.
4. Keep the WordPress hosting running until the new site is live, then cancel it.
