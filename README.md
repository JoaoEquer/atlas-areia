<p align="center">
  <img alt="Areia icon: sand dunes under a teal sun" src="areia/icon.png" width="96">
</p>

<h1 align="center">Areia</h1>

<p align="center">
  A warm, paper-like light theme for <a href="https://github.com/marqueskaio/atlas">Atlas</a>.<br>
  Sand grounds, ink-dark text, state colors tuned to match.
</p>

<p align="center">
  <a href="LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-8a846c"></a>
  <img alt="Atlas plugin API 24" src="https://img.shields.io/badge/atlas.api-24%2B-265493">
  <img alt="Contrast WCAG AA" src="https://img.shields.io/badge/contrast-WCAG%20AA-1f7f76">
  <img alt="Runs no code" src="https://img.shields.io/badge/runs%20code-no-1f7f76">
</p>

<p align="center">
  <img alt="Atlas with the Areia theme: a conversation with tool calls and a code diff on sand-colored paper" src="areia/screenshots/chat.png" width="880">
</p>

## Why

Atlas ships a light look and a dark one. The light one is stark white, which is hard on the eyes in
a bright room. Areia keeps the same layout and swaps the greys for warm neutrals, so the page reads
like paper under a lamp, with text kept dark enough to stay sharp.

| Default light | Areia |
|---|---|
| <img alt="Atlas with its default light look" src="areia/screenshots/default-light.png"> | <img alt="Atlas with Areia" src="areia/screenshots/chat.png"> |

The four states keep one meaning each and stay readable on sand: working, waiting for you, done
and failed.

<p align="center">
  <img alt="A conversation waiting for approval, with a finished and a failed tool call, and another conversation still working" src="areia/screenshots/states.png" width="880">
</p>

## Install

1. Open **Marketplace** in Atlas, find **Areia** under Plugins and press **Install**.
   From a terminal: `atlas marketplace install areia`.
2. Turn it on under **Plugins**. The consent shows one line: it adds a theme, and nothing that runs.
3. Choose it in **Settings > General > Look**, beside the system's, Light and Dark.

<p align="center">
  <img alt="Settings, Look: the system's, Light, Dark and Sand" src="areia/screenshots/settings.png" width="640">
</p>

In the app it is **Sand** in English and **Areia** in Portuguese. Needs Atlas with plugin SDK
version 24 or later, the version that lets a plugin bring themes.

## The palette

<img alt="Areia palette: background, sidebar, dialogs, chips, selected, text, and the four states" src="areia/screenshots/palette.png">

Atlas paints every screen with 27 named colors and no others. Areia sets all 27, so nothing falls
back to the default look. Every text color is at least **4.5:1** (WCAG AA) on the grounds it is
drawn on, and the main text reaches **13.5:1**. The full table, with each name, its value and the
measured contrast, is in [`areia/README.md`](areia/README.md#colors).

## Safe by design

A theme in Atlas is data, not code. Areia is one JSON file, [`themes/areia.json`](areia/themes/areia.json).

- **Runs nothing.** No Python, no screen, no hooks, no tools.
- **No network, no secrets,** and it touches nothing outside its own folder.
- **Can only paint.** Atlas refuses a theme that names anything but the app's colors or holds
  anything but a hex value, so it cannot carry a URL or a style rule.
- **Reversible.** Turn the plugin off and the app returns to the system's look. Your choice is kept
  for when it is back on.

## How it works

```
plugin.json  ──►  atlas.themes: ["areia"]   declared, shown at consent
themes/areia.json  ──►  27 named colors     validated by Atlas on load
Atlas desktop  ──►  --background, --soft…   set on the page root, over the light base
```

The plugin declares the theme in its manifest and Atlas validates the file when it loads the plugin.
The app sets each color as a CSS variable on the page root, on top of its light look, and takes
them off again when you pick another look.

## Repository

| Path | What it holds |
|---|---|
| [`areia/`](areia) | The plugin: manifest, theme, icon, screenshots, its own README and license |
| [`areia/themes/areia.json`](areia/themes/areia.json) | The colors |
| [`areia/README.md`](areia/README.md) | The plugin's page in Atlas: every color, the contrast table, design notes |
| [`areia/icon.svg`](areia/icon.svg) | Source of the Marketplace icon, `icon.png` (256x256) |
| [`CHANGELOG.md`](CHANGELOG.md) | What changed in each version |

Check it with Atlas installed:

```bash
atlas plugins validate areia
```

## License

MIT, see [LICENSE](LICENSE). Each plugin folder carries its own copy.
