# diver.today

One page for Rustam's five dive apps — Turn Pressure, Time to Surface, Weights Check, Surface
Interval and Dive log — with a full-width video of each app in action, its App Store link and one
line on what it is for. Built 2026-10-14 on his brief: *"a single page with full width videos of my
apps in action along with links to apple store … hosting for now shall be free, design shall be
crisp and super modern and without unnecessary elements"*, to bring in new users from forums
and search. **This file is the present tense; read it before changing anything.**

## What is where

| | |
|---|---|
| The page | `index.html` (one file, inline script), `style.css` (`?v=` on its link is the cache-buster: bump it when the CSS changes) |
| Media | `img/` icons at 512, favicon, `og.png` (1200×630), posters; `video/` ten MP4s, `<app>-wide.mp4` (1920×1080, desktops) and `<app>-tall.mp4` (864×1080, 4:5, phones) |
| Generator | `tools/build-media.py` — makes all of `img/` and `video/` from the app repositories beside this one. Needs ffmpeg and Pillow, both on this Mac. `build/` is its scratch, git-ignored |
| Hosting | GitHub Pages, repo `ligrimp-lang/diver-today`, branch `main`, folder `/`, no build step (`.nojekyll`). Push to `main` and it deploys in about a minute |
| Domain | `diver.today` at Namecheap. Advanced DNS holds four `A` records on `@` → 185.199.108.153 / .109 / .110 / .111 and `CNAME www` → `ligrimp-lang.github.io` (set by Rustam, 2026-10-14). The `CNAME` file in this repo tells GitHub the domain |
| Search | `robots.txt`, `sitemap.xml`, canonical `https://diver.today/`, JSON-LD `WebSite` + `ItemList` of five `SoftwareApplication`s, Open Graph and Twitter cards |
| Preview | `.claude/launch.json` starts `python3 -m http.server 8765` for the browser pane |

## The apps on the page

The App Store ids, store names and the per-app sites (each app's own repo publishes its landing,
privacy and support pages, which this page links to as "Details, support & privacy"):

| App | Store name | id | Per-app site |
|---|---|---|---|
| Turn Pressure | Turn Pressure – Dive Planner | 6801749776 | ligrimp-lang.github.io/turnpressure-site/ |
| Time to Surface | Time to Surface – Deco Planner | 6803187271 | ligrimp-lang.github.io/timetosurface-site/ |
| Weights Check | Weights Check – Dive Weighting | 6806640499 | ligrimp-lang.github.io/weightscheck-site/ |
| Surface Interval | Surface Interval – Dive Videos (iPhone and Mac, one record) | 6813333816 | ligrimp-lang.github.io/surfaceinterval-site/ |
| Dive log | Dive log – Computer Logbook | 6822452235 | ligrimp-lang.github.io/divelog-site/ |

Verify a listing with `curl "https://itunes.apple.com/lookup?id=<id>"` rather than from memory.
**Dive log went into App Review on 2026-10-14**; the page shows its button as "Coming soon on the
App Store" (class `soon` on the link, plus the `.note` under it). The link already points at the
store, so when Apple approves it, remove the class and the note — nothing else.

## Words on the page are the apps' approved words

The subtitle under each name is the App Store subtitle; the sentence is the App Store
promotional text (`docs/app-store-listing*.md` in each app's repo), lightly joined. The captions
inside the videos are the screenshot captions each app ships to the store
(`caption-screenshots.swift` in each repo's ship scripts). **Do not write new marketing claims
here** — change the listing in the app's repo first, then mirror it. The app is "Weights Check"
with the s, "Dive log" with a small l; these are his names.

Rules carried over from every app: copyright reads **Rustam Ismailov** and nothing else; no
invented company; British spelling in his own text, American only where it quotes the US store.

## How the videos are made (so they stay one family)

Each video is a title card (icon, name, tagline), one scene per store screenshot (the phone with
rounded corners and a shadow, drifting upward; a numbered teal pill, headline and subline), and
an outro ("Free on the App Store · diver.today"), over a blurred, darkened, slowed loop of two reef
clips from `surface_interval/reference-footage/clips/`. The look was taken from the Time to
Surface promo Rustam had made on 2026-10-10 (`turn_pressure/build/promo/`). Scenes and captions
are the `APPS` table at the top of the generator; the screenshots are read from each app's
`design/screenshots/<app>/` (1320×2868, the 6.9" set). Fonts are SF Pro from the system.

    python3 tools/build-media.py bg          # once, or when the background should change
    python3 tools/build-media.py icons       # icons, favicon, og.png
    python3 tools/build-media.py videos      # all ten videos and posters (~6 min)
    python3 tools/build-media.py videos dive-log   # one app

Then commit and push. Check a video by pulling frames with ffmpeg and looking at them; the
caption must never run under the phone (the wide layout keeps 820 px for a left caption).

## What was decided and why

- **GitHub Pages, not Cloudflare or Netlify** — free, already used by all five app sites, and the
  `gh` login on this Mac has the repo scope. One repo is both source and site; there is no
  separate publishing repo because this project *is* the site.
- **Generated videos, not screen recordings** — one consistent family for five apps in one
  session, regenerable in minutes when an app's screenshots change. The real screen recordings
  can replace them later by dropping files with the same names into `video/`.
- **Two cuts per video** — a 16:9 frame is unreadable at phone width, so phones get a 4:5 cut
  with the caption above the phone. The page picks the cut in its script by viewport width.
- **Videos load only when scrolled to**, muted, looping, and stop when scrolled away; with
  "reduce motion" set they wait for a tap. No analytics, no fonts from a CDN, no framework.
- **The custom domain and the first deploy** — GitHub's deploy health-checks the custom domain
  and times out after ten minutes while the domain still points at the registrar. The CNAME
  file was held back until the DNS was in, then restored. If a deploy ever fails with
  "in progress deployment", cancel the stuck one:
  `gh api -X POST repos/ligrimp-lang/diver-today/pages/deployments/<sha>/cancel`, then
  `gh run rerun <run-id> --failed`.

## Not done yet / next

- "Enforce HTTPS" in the Pages settings, once GitHub has issued the certificate for the domain
  (`gh api -X PUT repos/ligrimp-lang/diver-today/pages -F https_enforced=true`).
- Dive log's button when it is on sale (above).
- Submitting `https://diver.today/sitemap.xml` to Google Search Console is Rustam's, in his
  Google account; the page is ready for it.
