# Maintaining the website

The site is plain HTML, CSS and a little JavaScript: no build step, no frameworks, no cookies, no tracking, and
nothing loaded from other servers (a strict Content-Security-Policy enforces that).

```
index.html            the site
legal.html            risk disclosure, terms and privacy
404.html              not-found page
assets/css/site.css   all styles
assets/js/site.js     mobile menu, image viewer, footer year
assets/img/           logo, setup cards (WebP, 800 and 1600 px), social preview card (og-card-v2.jpg)
assets/brand/         README artwork: animated banner, metrics, roadmap, product icons (SVG)
favicon.svg  robots.txt  .nojekyll
```

## Hosting

GitHub Pages, from the `main` branch, root folder. Live at `https://cypherbird.github.io/intelradar-research/`.
The repository must stay public for free Pages hosting. If the address changes (another repository name, an
organisation or a custom domain), update the two `og:image` / `twitter:image` URLs at the top of `index.html`
so link previews on X and Telegram keep showing the card.

## Publishing a change

Edit the files, then in GitHub Desktop: write a summary → **Commit to main** → **Push origin**. Pages republishes
within about a minute.

## Replacing the setup cards

Cards come from the IntelRadar production server's `output/charts/`. Convert a new card to WebP at 1600 and 800 px
wide (quality ~84) and keep the same file names, or add a new `<figure class="shot">` block in `index.html` and a
matching cell in the README gallery.

## Updating the numbers

The metrics (setups published, coins in coverage) must be real: count them from the production server before
changing them, in `index.html`, `assets/brand/readme-metrics.svg` and the README.

## Content rules

Business-class research brand: lead with value, never with "not a scam" denials. Say "setups", never "calls" or
"free calls". No win-rate or profit claims; every result shown comes with its base rate or its stops. Motto:
"Clarity is freedom." / "Navigate open markets with evidence." Not financial advice.
