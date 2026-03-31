# Zellij Config

Personal Zellij setup with vim-style keybindings, locked mode as default, and a minimal compact layout.

## Theme

[Tokyo Night](https://github.com/folke/tokyonight.nvim) — defined in `themes/tokyo-night.kdl`.

## Layout

`layouts/compact.kdl` — a single main pane with a borderless `compact-bar` at the bottom (tooltip on `F1`).

## Key Concepts

- **Default mode: `locked`** — keypresses go directly to the terminal. Enter other modes explicitly.
- **`clear-defaults=true`** — all default Zellij keybindings are removed; only bindings below are active.
- **`on_force_close "quit"`** — closing the terminal window quits the session rather than detaching.

## Keybindings

### Global (all modes except `locked`)

| Key | Action |
|-----|--------|
| `Ctrl g` | Toggle locked ↔ current mode |
| `Ctrl q` | Quit |
| `Esc` / `Enter` | Return to locked mode |

### Mode Entry (from any non-locked mode)

| Key | Mode |
|-----|------|
| `p` | Pane |
| `t` | Tab |
| `r` | Resize |
| `m` | Move |
| `s` | Scroll |
| `o` | Session |

### Pane mode (`p`)

| Key | Action |
|-----|--------|
| `h/j/k/l` | Move focus left/down/up/right |
| `n` | New pane |
| `d` | New pane (down) |
| `r` | New pane (right) |
| `x` | Close focused pane |
| `f` | Toggle fullscreen |
| `z` | Toggle pane frames |
| `w` | Toggle floating panes |
| `e` | Embed or float focused pane |
| `c` | Rename pane |
| `Tab` | Switch focus |

### Tab mode (`t`)

| Key | Action |
|-----|--------|
| `h/k` | Previous tab |
| `j/l` | Next tab |
| `n` | New tab |
| `x` | Close tab |
| `r` | Rename tab |
| `s` | Toggle sync tab |
| `b` | Break pane to new tab |
| `[` / `]` | Break pane left/right |
| `1`–`9` | Go to tab N |

### Resize mode (`r`)

| Key | Action |
|-----|--------|
| `h/j/k/l` | Increase size left/down/up/right |
| `H/J/K/L` | Decrease size left/down/up/right |
| `+` / `=` | Increase size |
| `-` | Decrease size |

### Move mode (`m`)

| Key | Action |
|-----|--------|
| `h/j/k/l` | Move pane left/down/up/right |
| `n` / `Tab` | Move pane forward |
| `p` | Move pane backward |

### Scroll mode (`s`)

| Key | Action |
|-----|--------|
| `j/k` | Scroll down/up |
| `d/u` | Half-page down/up |
| `h/l` | Page up/down |
| `Ctrl f` / `Ctrl b` | Page down/up |
| `Ctrl c` | Scroll to bottom, return to locked |
| `f` | Enter search |
| `e` | Edit scrollback in `$EDITOR` |

### Search mode (entered from scroll with `f`)

| Key | Action |
|-----|--------|
| `n/p` | Next/previous result |
| `c` | Toggle case sensitivity |
| `w` | Toggle wrap |
| `o` | Toggle whole word |

### Session mode (`o`)

| Key | Action |
|-----|--------|
| `w` | Session manager |
| `c` | Configuration UI |
| `p` | Plugin manager |
| `d` | Detach |

### Always-on (normal + locked)

| Key | Action |
|-----|--------|
| `Alt h/j/k/l` | Move focus / switch tab |
| `Alt left/right/up/down` | Move focus / switch tab |
| `Alt n` | New pane |
| `Alt f` | Toggle floating panes |
| `Alt [` / `Alt ]` | Previous/next swap layout |
| `Alt +` / `Alt =` / `Alt -` | Resize increase/decrease |
| `Alt i` / `Alt o` | Move tab left/right |
