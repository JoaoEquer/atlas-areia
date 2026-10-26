# Areia

A light theme for [Atlas](https://github.com/marqueskaio/atlas): a warm paper look. The grounds
are sand, the text is ink-dark, the one accent is the app's own state colors tuned to sit on that
paper. In the settings it is called **Areia** in Portuguese and **Sand** in English.

## Use it

Install it from the app's **Marketplace** (or `atlas marketplace install areia`), turn it on in
**Plugins**, then pick it under **Settings > Theme**, beside the system's, light and dark.

## What it does

It brings one file, `themes/areia.json`: a hex color for each of the app's named colors
(`background`, `soft`, `raised`, `working`, `done` and the rest). Nothing else.

- It runs no code: no Python, no screen, no hooks.
- It reaches no network and reads no secret.
- It reads and writes nothing outside its own folder.

Turning it on shows exactly that: "Adds the themes areia: colors for the app, and nothing that
runs." Turn the plugin off and the app goes back to the system's look; your choice is kept for
when it is on again.

## The colors

Every text color keeps at least 4.5:1 contrast on the grounds it is drawn on (WCAG AA), measured
on `background`, `subtle`, `raised` and `muted`; `foreground` reaches 13.5:1. `faint` only
decorates, as the app says of it, and is below that on purpose.

| Name | Color | Use |
|---|---|---|
| `background` | `#e9e3d3` | the page |
| `foreground` | `#1c1b17` | the text |
| `subtle` | `#e0d9c6` | the sidebar and side panels |
| `raised` | `#f1ecdf` | dialogs, menus, fields |
| `working` / `done` / `failed` | `#265493` / `#1f7f76` / `#b8352a` | the states |

Needs Atlas with plugin SDK version 24 (`atlas.api` 24) or later.

## License

MIT.
