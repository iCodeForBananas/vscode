# iCodeForBananas for VS Code

A VS Code color theme in two variants — **iCodeForBananas Dark** and **iCodeForBananas Light** — ported from the iTerm2 color schemes of the same name.

## Install

### From source

```bash
git clone <this-repo> ~/vscode-themes/icodeforbananas
ln -s ~/vscode-themes/icodeforbananas ~/.vscode/extensions/icodeforbananas-theme-1.0.0
```

Restart VS Code, then **Cmd+K Cmd+T** (macOS) / **Ctrl+K Ctrl+T** and pick a variant.

### Package a `.vsix`

```bash
npx @vscode/vsce package
code --install-extension icodeforbananas-theme-1.0.0.vsix
```

## What came from the iTerm2 schemes

These values are carried over exactly:

| Role | Dark | Light |
|---|---|---|
| Editor background | `#0F1114` | `#FDFCFA` |
| Editor foreground | `#E6E8EB` | `#0A0C0E` |
| Cursor | `#FFCC00` | `#755000` |
| Selection | `#27456B` | `#BBD6F5` |
| Current-line highlight | `#1B1E23` | `#F1EEE6` |

All 16 ANSI colors map straight onto the integrated terminal, so a shell inside VS Code matches iTerm2 exactly.

### ANSI palette

| | Dark | Dark bright | Light | Light bright |
|---|---|---|---|---|
| Black | `#98A2B0` | `#B3BCC8` | `#16181C` | `#6E757E` |
| Red | `#FF8A82` | `#FFA198` | `#C21F2E` | `#E0132A` |
| Green | `#6FD28A` | `#7EE787` | `#157A34` | `#008736` |
| Yellow | `#E3B341` | `#F2CC60` | `#8A5A00` | `#A26800` |
| Blue | `#79B8FF` | `#A5D6FF` | `#0B5FD0` | `#006FF1` |
| Magenta | `#D2A8FF` | `#E2C5FF` | `#8A33C8` | `#A526F0` |
| Cyan | `#56D4DD` | `#76E3EA` | `#0D7478` | `#008288` |
| White | `#F2F6FA` | `#FFFFFF` | `#3F464E` | `#000000` |

## What was derived

An iTerm2 scheme only defines 16 ANSI colors plus a handful of UI slots, so the rest is extrapolated from that palette:

- **Workbench chrome** — sidebar, tabs, status bar, widgets, borders: neutral steps built off the background.
- **Syntax tokens** — mapped GitHub-style, since the palette is clearly GitHub-derived: red = keyword/storage, blue = string, magenta = function, cyan = type/class, yellow = parameter/property, gray = comment, bright blue = constant/number, green = markup tag.
- **Diagnostics and git decorations** — red = error/deleted, yellow = warning/modified, green = added, blue = info.

## Layout

```
package.json
themes/
  icodeforbananas-dark-color-theme.json
  icodeforbananas-light-color-theme.json
```

Edit a theme file and reload the window (**Cmd+R** in the Extension Development Host, or **Developer: Reload Window**) to see changes.

## License

MIT — see [LICENSE](LICENSE).
