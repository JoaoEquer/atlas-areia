# Changelog

All notable changes to Areia are listed here. The format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and the project uses
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.2.0]

### Added

- Two dark themes in the same plugin, each setting all 27 named colors on top of `dark`:
  - **Coffee** (`themes/cafe.json`, Café in Portuguese): Areia's night twin, espresso grounds and
    cream text, the same warm hue family.
  - **Graphite** (`themes/grafite.json`, Grafite in Portuguese): a cool near-black with electric
    cyan for working and focus, mint for done.
- Every text color of both themes is at least 4.5:1 (WCAG AA) on the four text grounds.
- Screenshots at 1440x900 (rendered at 2x), the same scenes as Areia's: a working conversation
  with a diff, the four states and Settings, for each theme (`cafe-*.png`, `grafite-*.png`), and
  the scene in the default dark look (`default-dark.png`).
- Both READMEs show the dark themes.

Areia's colors are unchanged.

## [1.1.0]

### Added

- A square icon for the Marketplace, `areia/icon.png` (256x256), drawn in the theme's own colors
  from `areia/icon.svg`.
- `areia/screenshots/states.png`: the working, waiting, done and failed states on sand.
- `areia/screenshots/palette.png`, a raster copy of the palette for pages that do not show SVG.
- This changelog.

### Changed

- New screenshots at 1440x900 (rendered at 2x): a working conversation with tool calls and a code
  diff, the same scene in the default light look, and Settings with Sand chosen.
- The plugin's README is reorganized as its page in Atlas: pitch, before and after, what it
  changes and what it doesn't, install in three steps, safety, palette and contrast.

The theme's colors are unchanged.

## [1.0.0]

### Added

- First release: the Sand look (Areia in Portuguese), 27 named colors on top of Atlas's light
  look, declared through `atlas.themes` with plugin SDK version 24.

[1.2.0]: https://github.com/JoaoEquer/atlas-areia/compare/d6dc977...main
[1.1.0]: https://github.com/JoaoEquer/atlas-areia/compare/7856d50...d6dc977
[1.0.0]: https://github.com/JoaoEquer/atlas-areia/tree/7856d506794f1254ee7915e6595ec05eb76e803d
