# بين السطور · Hidden Layers of Truth

A browser mystery in Tunisian Darja. This repository contains the standalone game, including the story, save system, original artwork and synthesized soundtrack.

## Development

Use Node.js 24.

```sh
npm ci
npm run dev
```

## Verify

```sh
npm test
npm run build
npx playwright install chromium --only-shell
npm run test:browser
```

The browser suite exercises all endings across four viewport sizes. Set `CHROMIUM_BIN` to use an installed Chromium, or `GAME_TEST_PREFIX=/example/` to test a project URL. The build uses relative asset URLs and publishes from `dist/`.

The game saves progress in the browser for the current origin. Its optional Qur’an recitation streams from EveryAyah.

## Playtest feedback

The ending submits anonymous responses to the Baynasotour feedback service. The
service writes to the private `feedback` table in the Sites project named
**Baynasotour feedback**. It exposes a public write endpoint for the game domain
and no public read endpoint. The owner can inspect the responses through Sites.
