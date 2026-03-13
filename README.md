# pi-redraw-screen

Force a full screen redraw in **pi** via a slash command and optional shortcut.

## Features

- `/redraw` command for forced full TUI redraw (`requestRender(true)`)
- Optional keyboard shortcut (default: `ctrl+r`)
- Shortcut configurable via pi settings:
  - `redraw_shortcut` (preferred)
  - `redrawShortcut` (fallback)
- Disable shortcut by setting it to `false`, `""`, or `"none"`

## Shortcut configuration

Set in either:

- Project: `.pi/settings.json`
- Global: `~/.pi/agent/settings.json`

Project setting takes precedence over global.

```json
{
  "redraw_shortcut": "ctrl+r"
}
```

Disable shortcut:

```json
{
  "redraw_shortcut": false
}
```

## Local usage

From this folder:

```bash
cd /Users/user/code/pi-redraw-screen
pi -e ./extensions/pi-redraw-screen.ts
```

Then in pi:

```text
/redraw
```

## Install as a package

```bash
pi install git:github.com/memgrafter/pi-redraw-screen
# pinned
pi install git:github.com/memgrafter/pi-redraw-screen@v0.1.0
```

Project-local install:

```bash
pi install -l git:github.com/memgrafter/pi-redraw-screen
```
