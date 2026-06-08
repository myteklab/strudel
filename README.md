# Strudel (MYTEK Lab integration)

Platform wrapper for [Strudel](https://strudel.cc) — live-coding music in the browser
(TidalCycles patterns in JavaScript). Upstream source: <https://codeberg.org/uzu/strudel>
(AGPL-3.0). This repo does **not** contain Strudel's source; it vendors the prebuilt,
self-contained REPL bundle plus our integration assets.

## Contents

- `strudel-repl.js` — the prebuilt `@strudel/repl` web-component bundle (defines
  `<strudel-editor>`). ~2.2 MB, self-contained (no build step on our side).
- `icon.png` — app icon.

## Not in this repo (injected by the platform at runtime)

- `platform.html` — the iframe wrapper (gitignored). Adds the Play/Stop bar, the
  instant code preview, the Examples dropdown, and loads `strudel-repl.js`.
- `platform-adapters/strudel-adapter.js` — save/load + transport + examples wiring.

## Updating the bundle

The bundle is the published `@strudel/repl` package. To refresh:

```
curl -L https://unpkg.com/@strudel/repl/dist/index.js -o strudel-repl.js
```

Then test in the `--dev` worktree before deploying to `apps/strudel/`.

## License

Strudel is AGPL-3.0. We self-host an unmodified copy of the published bundle.
