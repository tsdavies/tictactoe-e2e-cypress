# tictactoe-e2e-cypress — Vanilla JS Tic-Tac-Toe (Cypress E2E · Travis CI)

[![Build Status](https://app.travis-ci.com/tsdavies/tictactoe-e2e-cypress.svg?branch=main)](https://app.travis-ci.com/github/tsdavies/tictactoe-e2e-cypress)

A small, **framework-free** web app that showcases front-end fundamentals with a reproducible **Cypress** end-to-end test suite running in **Travis CI**. Built as a compact, reviewer-friendly portfolio piece.

**Live site:** https://tsdavies.github.io/tictactoe-e2e-cypress/

![Cypress](https://user-images.githubusercontent.com/31829478/104397633-206c3980-5545-11eb-95b6-38abce4f4202.gif "")

---

## Why this repo (for hiring managers)

- **Vanilla JS, HTML, CSS:** No scaffolds or frameworks—just the core web platform.
- **Real tests:** Cypress specs exercise real user journeys (win, draw, reset).
- **CI automation:** Tests run headless in **Travis CI**, surfacing a clean pass/fail signal on each commit.
- **Portable:** Static files; easy to host (GitHub Pages) and easy to run locally.

---

## Quick tour — what to review

- **`index.html`** — semantic markup and simple layout.
- **`css/…`** — small, focused stylesheets.
- **`scripts/app.js`** — vanilla JS for board state & interactions.
- **`cypress/…`** — end-to-end specs asserting visible outcomes.
- **`.travis.yml`** — minimal CI config that runs Cypress against a target URL.

---

## Project structure

```
.
├─ index.html
├─ css/
│  ├─ style.css
│  ├─ nav.css
│  ├─ article.css
│  ├─ media-queries.css
│  └─ fonts-and-text.css
├─ scripts/
│  └─ app.js
├─ images/
├─ cypress/
│  ├─ e2e/            # test specs
│  ├─ fixtures/
│  └─ support/
├─ cypress.config.*   # may vary by Cypress version
└─ .travis.yml
```

---

## Getting started (local)

No build step required. Any static server works.

```sh
npm start
```

Alternative local servers:

```sh
# Node (no install)
npx serve .
```

Then visit `http://localhost:8000`.

---

## Testing

**Headless (CI-style):**

```sh
npm test
```

**Interactive runner:**

```sh
npm run test:ui
```

**Run Cypress directly against local or deployed URLs:**

```sh
# Headed (local)
npx cypress open --config baseUrl=http://localhost:8000

# Headless (local)
npx cypress run  --config baseUrl=http://localhost:8000

# Headed (deployed)
npx cypress open --config baseUrl=https://tsdavies.github.io/tictactoe-e2e-cypress/

# Headless (deployed)
npx cypress run  --config baseUrl=https://tsdavies.github.io/tictactoe-e2e-cypress/
```

---

## Continuous Integration (Travis CI)

Travis installs dependencies and runs the Cypress suite headless. The badge at the top reflects build status.

---

## Licence & attribution

- Vanilla JS source © TS Davies 2025. Educational/Training use.
- Typeface: Google Fonts **Questrial**.
