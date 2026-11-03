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
