# pi-redraw-screen

Force a full screen redraw in **pi** via a slash command and optional shortcut.

## Features

- `/redraw` command for forced full TUI redraw (`requestRender(true)`)
- Optional keyboard shortcut (no default — opt-in via settings)
- Shortcut configurable via pi settings:
  - `redraw_shortcut` (preferred)
  - `redrawShortcut` (fallback)
- Disable shortcut by setting it to `false`, `""`, or `"none"`

## Shortcut configuration

Set in either:

- Project: `.pi/settings.json`
- Global: `~/.pi/agent/settings.json`

Project setting takes precedence over global.

### Enable `ctrl+r`

**1. Bind the shortcut** in `~/.pi/agent/settings.json`:

```json
{
  "redraw_shortcut": "ctrl+r"
}
```

**2. Rebind `renameSession`** in `~/.pi/agent/keybindings.json` to avoid the
built-in conflict warning:

```json
{
  "renameSession": ["ctrl+shift+r"]
}
```

### Disable shortcut

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
