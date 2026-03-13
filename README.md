# pi-redraw-screen

Force a full screen redraw in **pi** via a slash command and optional shortcut.

## Features

- `/redraw` command for forced full TUI redraw (`requestRender(true)`)
- Optional keyboard shortcut (no default — opt-in via settings)

## Shortcut configuration

To bind a keyboard shortcut, add to `~/.pi/agent/settings.json` (global) or
`.pi/settings.json` (project-local, takes precedence):

```json
{
  "redraw_shortcut": "ctrl+r"
}
```

If binding `ctrl+r`, also rebind `renameSession` in `~/.pi/agent/keybindings.json`
to avoid the built-in conflict warning:

```json
{
  "renameSession": ["ctrl+shift+r"]
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
