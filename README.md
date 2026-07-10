# The GOAT Gamble

Source for **[thegoatgamble.com](https://thegoatgamble.com)** — a small collection of free
browser games, playable with no sign-up and no downloads. Static site, deployed via GitHub Pages.

## Games

| Game | File | About |
|------|------|-------|
| ♟️ Chess | `chess.html` | Full standard rules vs. a 3-level computer or 2-player hotseat. Clock, sound, captured-pieces tray; move generation is perft-verified. |
| 🔴 Connect Four | `connect_four.html` | Drop discs vs. an alpha-beta AI with three difficulties and a match scoreboard. |
| 🃏 Blackjack | `blackjack.html` | 6-deck shoe, 3:2 payouts, split & double, with a built-in basic-strategy coach. |
| 🧊 Tri-D Chess | `tri_d_chess.html` | Star-Trek-style 3D chess on stacked boards with movable attack boards. |
| ⚡ Neon Dash | [external](https://ebarber79.github.io/license.md/) | Neon endless runner — jump & dash, bank your gems. Also ships as a mobile app. |

Each game is a **single self-contained HTML file** — no build step, no external/CDN
dependencies, so they run offline and can be added to a phone's home screen.

## Structure

```
index.html            Landing page / hub (SEO, Open Graph, JSON-LD, PWA manifest link)
*.html                The four house games (one file each)
icons/                Card icons (.png) + Neon Dash icon (.svg)
og.png                1200×630 social-share preview image
qr.png                QR code to thegoatgamble.com
manifest.webmanifest  PWA manifest (installable hub)
sitemap.xml, robots.txt
CNAME                 Custom domain for GitHub Pages
.nojekyll             Serve files as-is (skip Jekyll processing)
```

## Local preview

No tooling required — open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Hosted on **GitHub Pages** from the `main` branch (root), with the custom domain
`thegoatgamble.com` set via the `CNAME` file. Pushing to `main` publishes the site.

## License

© The GOAT Gamble. All game code and assets are original.
