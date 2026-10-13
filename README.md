# IntelRadar Research — website

The public website for IntelRadar Research: what we do, how a call is made, real cards, research standards,
the Free and Pro tiers, and links to Telegram and X.

Plain HTML, CSS and a little JavaScript. No build step, no frameworks, no cookies, no tracking, and nothing loaded
from other servers (a strict Content-Security-Policy enforces that).

```
index.html            the site
legal.html            risk disclosure, terms and privacy
404.html              not-found page
assets/css/site.css   all styles
assets/js/site.js     mobile menu, screenshot viewer, footer year
assets/img/           logo, product cards (WebP, 800 and 1600 px), social preview (og-card.jpg)
favicon.svg  robots.txt  .nojekyll
```

## Publish free on GitHub Pages (with GitHub Desktop)

1. GitHub Desktop → **File → Add local repository** → choose this folder.
2. **Publish repository**. Name it `intelradar-research` and **untick "Keep this code private"**:
   free GitHub Pages needs a public repository. The site contains no secrets.
3. On github.com, open the repository → **Settings → Pages** → Source **Deploy from a branch** →
   Branch **main**, folder **/ (root)** → **Save**.
4. After a minute the site is live at `https://cypherbird.github.io/intelradar-research/`.

If the address is different (another repository name, an organisation, or your own domain), change the two
`og:image` / `twitter:image` URLs at the top of `index.html` so link previews on X and Telegram show the card.

## Update the site

Edit the files, then in GitHub Desktop: write a summary → **Commit to main** → **Push origin**. Pages republishes
within about a minute.

## Replacing the screenshots

Cards come from the IntelRadar server's `output/charts/`. Convert a new card with Pillow to WebP at 1600 and 800 px
wide (quality ~84) and keep the same file names, or add a new `<figure class="shot">` block in `index.html`.

## Content rules

Research, not hype: no win-rate or profit claims, no "VIP", no urgency. Every result shown must come with its base
rate or its stops. Not financial advice.
