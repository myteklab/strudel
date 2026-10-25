# Strudel, as served on mytekdev.com

[Strudel](https://strudel.cc) is live coding for music in the browser, a JavaScript
take on TidalCycles patterns, by Felix Roos, Alex McLean and contributors. It is
licensed under the GNU Affero General Public License v3 or later, and so is
everything here (see LICENSE).

This repository holds the copy that students open on mytekdev.com. Nothing in it is
modified:

- `strudel-repl.js` is `dist/index.js` from the npm package
  [@strudel/repl 1.3.0](https://www.npmjs.com/package/@strudel/repl/v/1.3.0),
  byte for byte. Its source is upstream commit
  [f610965f43](https://codeberg.org/uzu/strudel/src/commit/f610965f4332837febe45743105da170e8b331ed)
  (2026-01-17), tagged `@strudel/repl@1.3.0`.
- `icon.png` is upstream's `website/public/icon.png` from the same commit.

## Checking it

```
npm pack @strudel/repl@1.3.0
tar -xzf strudel-repl-1.3.0.tgz
cmp package/dist/index.js strudel-repl.js
```

The page that loads the editor and the script that connects it to mytekdev.com
(Play and Stop buttons, the examples menu, saving) are separate programs that use
the `<strudel-editor>` element from outside. They are not part of this repository.
