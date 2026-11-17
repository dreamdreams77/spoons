# Spoons

A drawer for the energy you've got today.

Each morning, pick how many spoons you have. Things you plan cost spoons; some things give a spoon back. If the day is overbooked, move something to tomorrow. Close the day and what you did goes in the jar. After a few days, Patterns shows what your weeks tend to look like.

## Install

Open the site on your phone, then **Share → Add to Home Screen** (iOS) or **⋮ → Install app** (Android). After the first load it works fully offline.

## How it's built

- One `index.html`, vanilla JS, no framework, no build step
- State in `localStorage` under `spoons.v1`, with versioned migrations
- Service worker (`sw.js`) caches the app shell and fonts, network-first so updates arrive
- Light and dark themes from one token set; Auto follows `prefers-color-scheme`
- Respects `prefers-reduced-motion`; haptics via `navigator.vibrate` where supported
- No accounts, no analytics, no network calls after first load

## Fonts

[Bricolage Grotesque](https://github.com/ateliertriay/bricolage) and [Fraunces](https://github.com/undercasetype/Fraunces), subset to Latin and served locally. Both are under the SIL Open Font License; see `fonts/`.
