# bit-age-app-scripts

Small repository containing minified embed scripts and a GitHub Action to purge jsDelivr CDN.

## Files

- [script.develop.min.js](script.develop.min.js)
- [script.staging.min.js](script.staging.min.js)
- [script.min.js](script.min.js)
- [script.local.min.js](script.local.min.js)
- [.github/workflows/purge-cdn.yml](.github/workflows/purge-cdn.yml)

## CDN links (working)

- Develop:
  https://cdn.jsdelivr.net/gh/Black-Ink-Technologies/bit-age-app-scripts@1.x.x/script.develop.min.js

- Staging:
  https://cdn.jsdelivr.net/gh/Black-Ink-Technologies/bit-age-app-scripts@1.x.x/script.staging.min.js

- Production:
  https://cdn.jsdelivr.net/gh/Black-Ink-Technologies/bit-age-app-scripts@1.x.x/script.min.js

## CDN purge links

- Develop purge URL:
  https://purge.jsdelivr.net/gh/Black-Ink-Technologies/bit-age-app-scripts@1.x.x/script.develop.min.js

- Staging purge URL:
  https://purge.jsdelivr.net/gh/Black-Ink-Technologies/bit-age-app-scripts@1.x.x/script.staging.min.js

- Production purge URL:
  https://purge.jsdelivr.net/gh/Black-Ink-Technologies/bit-age-app-scripts@1.x.x/script.min.js

(Used by the workflow's `CDN_URL` in [.github/workflows/purge-cdn.yml](.github/workflows/purge-cdn.yml).)

## How it works

The GitHub Action at [.github/workflows/purge-cdn.yml](.github/workflows/purge-cdn.yml) issues a GET to the purge endpoint when commits are pushed to the corresponding branch. See the develop script at [script.develop.min.js](script.develop.min.js) for the develop build currently referenced by the purge URL.
