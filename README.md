# Cita iTerm themes

A light and dark color pair for iTerm2. The colors come from the Cita themes for Marta and its built-in terminal.

- `CitaDark.itermcolors`
- `CitaLight.itermcolors`

## Import

1. Open iTerm2 Settings → Profiles → Colors.
2. Click Color Presets… → Import….
3. Pick both files.

Bold text is mint. iTerm uses that color only when the Bold checkbox next to the color is on in the Colors tab.

## Use one profile that follows macOS

1. Pick a profile and open the Colors tab.
2. Check "Use different colors for light mode and dark mode".
3. In the Light tab, choose Cita Light from Color Presets….
4. In the Dark tab, choose Cita Dark.

iTerm now switches colors when macOS switches appearance.

## Use two separate profiles

1. Duplicate a profile twice. Name them "Cita Light" and "Cita Dark".
2. In each one, uncheck "Use different colors for light mode and dark mode".
3. Apply the matching preset.

## Test

Run this to see all 16 colors:

```sh
for i in {0..15}; do printf "\e[48;5;${i}m  \e[0m"; done; echo
```

## Unreadable colors

Some tools ignore the 16 preset colors and use fixed 256-color or true colors. iTerm can't change those, so they can be hard to read on Cita Light.

lsd does this by default. Use [lsd-theme](https://github.com/maliMirkec/lsd-theme) to fix it. It maps lsd colors to the 16 preset colors, so lsd follows Cita Light and Cita Dark.

For other tools, raise "Minimum contrast" in Settings → Profiles → Colors. It's a profile setting, so the preset files can't store it.

## Where the colors come from

The base colors come from the etty themes in `marta-themes`:

- `CitaLight.ettyTheme` → `CitaLight.itermcolors`
- `CitaDark.ettyTheme` → `CitaDark.itermcolors`

Keys map like this:

| etty | iTerm |
| --- | --- |
| `background` | Background Color |
| `foreground` | Foreground Color |
| `selection` | Selection Color |
| `selectedText` | Selected Text Color |
| `caret` | Cursor Color |
| `caretText` | Cursor Text Color |
| `ansiColors` | Ansi 0–15 Color |

## Mint extras

iTerm has a few colors etty doesn't have. They use Cita mint:

| Color | Light | Dark |
| --- | --- | --- |
| Bold Color | `#0a7f5a` | `#63f2c5` |
| Link Color | `#0a7f5a` | `#63f2c5` |
| Cursor Guide Color | `#0a7f5a` | `#63f2c5` |

The dark Selection Color is `#0f6652`, not the etty `#1a535e`. It gives more contrast in iTerm.

## Related

- `marta-themes` has the Marta and etty themes. Its config opens iTerm2 as the terminal.
- `herdr-theme` has the Herdr themes with the same base colors.
- [lsd-theme](https://github.com/maliMirkec/lsd-theme) has lsd colors that follow these presets.
