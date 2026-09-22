# erbasstudios.github.io

Public website of **Erbas Studios**, served by GitHub Pages at <https://erbasstudios.github.io>.
It holds only public, store-facing pages: the studio landing page, each game's privacy policy and
`app-ads.txt`. **Game source code does not live here** — every game has its own private repository
(`erbasstudios/yumo`, `erbasstudios/rainroutes`, …).

## Layout

```
/
├── index.html            Studio landing page — one card per game
├── 404.html              Not-found page + forwards moved URLs (see below)
├── app-ads.txt           AdMob publisher verification — MUST stay at the site root
├── assets/
│   └── site.css          Shared styles for every page
├── yumo/
│   └── privacy.html      Yumo privacy policy (English, then Turkish at #tr)
└── rainroutes/
    └── privacy.html      Rain Routes privacy policy
```

## Adding a new game

1. Create a folder named after the game in lowercase, no spaces: `/<game>/`.
2. Add `/<game>/privacy.html` (copy `yumo/privacy.html` as a template, link `/assets/site.css`).
3. Add a `.game` card to `index.html`.
4. Put `https://erbasstudios.github.io/<game>/privacy.html` into Play Console / App Store Connect.

## Rules

- **English file and folder names.** URLs appear in store listings worldwide. Page content is English
  first; other languages follow on the same page with an anchor (e.g. `#tr`).
- **`app-ads.txt` never leaves the root.** The IAB standard looks for it at `https://<domain>/app-ads.txt`.
  The publisher ID inside is shared by all games.
- **A published URL must keep working.** Stores and older app versions keep linking to it. When a page
  moves, add the old path to the `moved` map in `404.html` (e.g. `/gizlilik.html` → `/yumo/privacy.html`),
  then update the store listing.
- **Each game has its own policy.** Games collect different data; a shared policy would be inaccurate.
- **Keep policies true.** A policy must describe what the current app version actually does.

## Custom domain

If a domain (e.g. `erbasstudios.com`) is bought: Settings → Pages → Custom domain. The layout stays the
same; update the developer website in AdMob and the privacy URLs in the store listings.
