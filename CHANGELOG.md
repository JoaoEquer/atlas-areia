# Changelog

All notable changes to Areia are listed here. The format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and the project uses
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.3.0]

### Removed

- Coffee and Graphite, the two dark themes 1.2.0 brought, moved out to plugins of their own, each
  with its own Marketplace card: [Café](https://github.com/JoaoEquer/atlas-cafe) and
  [Grafite](https://github.com/JoaoEquer/atlas-grafite). Install the one you used; until then the
  app shows the system's look and keeps your choice.

Areia's colors are unchanged.

## [1.2.0]

### Added

- Two dark themes in the same plugin, Coffee and Graphite, with their screenshots.

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

[1.3.0]: https://github.com/JoaoEquer/atlas-areia/compare/8827648...main
[1.2.0]: https://github.com/JoaoEquer/atlas-areia/compare/d6dc977...8827648
[1.1.0]: https://github.com/JoaoEquer/atlas-areia/compare/7856d50...d6dc977
[1.0.0]: https://github.com/JoaoEquer/atlas-areia/tree/7856d506794f1254ee7915e6595ec05eb76e803d
