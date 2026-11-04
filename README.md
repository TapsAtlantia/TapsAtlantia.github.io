# Quantum Apps

The site at **[tapsatlantia.github.io](https://tapsatlantia.github.io/)** — a download page for
the Quantum Android apps.

- **[Quantum MTG](https://github.com/TapsAtlantia/QuantumMTG)** — Moxfield, TCGplayer and
  XMage Nexus in one app, with ad and popup blocking.
- **[QuantumManga](https://github.com/TapsAtlantia/QuantumManga)** — seven manga, light-novel
  and fanfic sites in one app, with ad and popup blocking.

Every app listed here was written by AI (Claude Code), and so was this page. The source for
each one is public.

## Adding an app

Everything on the page is driven by the `APPS` array near the bottom of `index.html`:

```js
{
  id: "mtg",                       // anchor id of its detail section
  name: "Quantum MTG",
  kind: "MAGIC: THE GATHERING",    // small label above the name
  repo: "QuantumMTG",              // GitHub repo under TapsAtlantia
  apk: "QuantumMTG.apk",           // asset name in the latest release
  icon: "assets/mtg/icon.png",
  blurb: "..."                     // one line, what it does
}
```

Add an object, drop a 512px icon in `assets/<id>/icon.png`, and write a matching
`<section class="app" id="<id>">` with its feature list. Version and APK size are pulled live
from the GitHub releases API, so they never need editing.

Pages serves this from the repository root on the default branch.
