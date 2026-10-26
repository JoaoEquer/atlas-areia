# Areia

A warm, paper-like light theme for [Atlas](https://github.com/marqueskaio/atlas). Sand grounds,
ink-dark text and state colors tuned to sit on that paper: a calmer alternative to the stark white
of the default light look, for working in daylight.

In the app's settings it is called **Sand** in English and **Areia** in Portuguese.

| Atlas, light (default) | Atlas, Areia |
|---|---|
| ![Atlas with its default light look](screenshots/default-light.png) | ![Atlas with Areia](screenshots/chat.png) |

![Settings, Look: the system's, Light, Dark and Sand](screenshots/settings.png)

## Install

From the app, open **Marketplace**, find **Areia** under Plugins and press **Install**. From a
terminal:

```bash
atlas marketplace install areia
atlas plugins enable areia
```

A plugin arrives turned off. Turning it on shows what it declares, which here is one line: it adds
a theme, and nothing that runs. Then choose it in **Settings > General > Look**, beside the
system's, Light and Dark.

Needs Atlas with plugin SDK version 24 (`atlas.api` 24) or later, the version that lets a plugin
bring themes.

## What it does

It brings one file, [`themes/areia.json`](themes/areia.json): a hex color for each of the app's
named colors, on top of the app's light look. Nothing else.

- **It runs no code.** No Python, no screen, no hooks, no tools, no scripts.
- **It reaches no network** and reads no secret.
- **It touches nothing outside its own folder.**
- **It cannot paint anything but the app's named colors.** Atlas refuses a theme that names any
  other variable or holds anything that is not a hex color, so a theme is data and cannot carry a
  URL or a style rule.

If you turn the plugin off, the app goes back to the system's look and keeps your choice for when
the plugin is on again.

## Colors

Atlas paints every screen with 27 named colors and no others; this theme sets each of them, so
nothing falls back to the default light look. The theme sits on `light`, which keeps native form
controls and scrollbars in their light variants.

**Grounds**

| Name | Color |
|---|---|
| `background` | `#e9e3d3` |
| `subtle` | `#e0d9c6` |
| `raised` | `#f1ecdf` |
| `muted` | `#dcd4bf` |
| `hover` | `#d9d1bb` |
| `selected` | `#d2c9b2` |
| `scrim` | `#1c1b1766` |

**Text**

| Name | Color |
|---|---|
| `foreground` | `#1c1b17` |
| `soft` | `#4b4940` |
| `muted-foreground` | `#55524a` |
| `faint` | `#8a846c` |

**Lines and focus**

| Name | Color |
|---|---|
| `border` | `#cbc2aa` |
| `border-strong` | `#b3a98f` |
| `ring` | `#6d6a5c` |

**Actions**

| Name | Color |
|---|---|
| `primary` | `#1c1b17` |
| `primary-foreground` | `#f1ecdf` |

**States**

| Name | Color |
|---|---|
| `working` | `#265493` |
| `waiting` | `#c98f23` |
| `waiting-text` | `#6e4a00` |
| `waiting-foreground` | `#3a2808` |
| `done` | `#1f7f76` |
| `done-text` | `#115a54` |
| `failed` | `#b8352a` |
| `failed-text` | `#8f261c` |
| `danger` | `#b8352a` |
| `added` | `#1f7f76` |
| `removed` | `#b8352a` |

### Contrast

Every text color is at least 4.5:1 (WCAG AA) on the four grounds a screen draws text on. The ratios
below were computed from the hex values with the WCAG relative-luminance formula; `foreground` on
`background` reaches 13.5:1.

| Text color | on `background` | on `subtle` | on `raised` | on `muted` |
|---|---|---|---|---|
| `foreground` `#1c1b17` | 13.5 | 12.2 | 14.6 | 11.7 |
| `soft` `#4b4940` | 7.0 | 6.4 | 7.7 | 6.1 |
| `muted-foreground` `#55524a` | 6.1 | 5.5 | 6.6 | 5.3 |
| `working` `#265493` | 5.9 | 5.4 | 6.4 | 5.1 |
| `waiting-text` `#6e4a00` | 6.2 | 5.6 | 6.7 | 5.4 |
| `done-text` `#115a54` | 6.3 | 5.7 | 6.8 | 5.4 |
| `failed-text` `#8f261c` | 6.7 | 6.1 | 7.2 | 5.8 |

`faint` only decorates (a chevron, a dot at rest, a word that cannot be used, as Atlas defines it)
and is 2.9:1 on `background` on purpose. `ring`, the keyboard's place, is 4.2:1. `border` and
`border-strong` are edges, not text, at 1.4:1 and 1.8:1: quiet lines on paper.

## Design

- **Warm neutrals.** Every neutral leans yellow-brown (OKLCH hue between 89 and 97 degrees, chroma 0.01 to 0.03) instead of
  gray: `background` is `#e9e3d3`, the sidebar a step darker, and dialogs and fields a
  step lighter (`raised`), so depth reads as paper laid over paper.
- **Ink, not black.** Text is `#1c1b17`, a very dark warm brown, which sits softer on sand
  than pure black.
- **States stay legible.** Blue, amber, green and red are the app's four states with one meaning
  each. Their `-text` variants are darkened until they read as words on sand.

## Develop

```bash
atlas plugins validate areia     # loads it as Atlas does and says what is wrong
```

The folder name must equal the plugin's `name`, as Atlas requires. To try a change, copy the folder
into your home's `plugins/`, run `atlas plugins enable areia`, and pick the theme in Settings.

## License

MIT, see [LICENSE](LICENSE).
