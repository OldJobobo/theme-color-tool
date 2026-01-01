# Theme Color Tool

Applies a Base16 YAML scheme to the theme files in the current directory.

This script is intended to be run from inside a theme repo.
It rewrites each supported file in place using the Base16 `base00`-`base0F` values
from the scheme.

## Usage

```bash
# run from inside a theme directory
python3 apply-theme.py -s <Your Base16 Scheme>.yaml
```

## Options

- `-s`, `--scheme` Path to a Base16 YAML scheme file (must include `base00`-`base0F`).
- `-q`, `--quiet`  Suppress per-file reporting.

## Supported Files

Terminal + shell:
- `ghostty.conf`
- `alacritty.toml`
- `kitty.conf`
- `warp.yaml`
- `colors.fish`
- `fzf.fish`
- `vencord.theme.css`

Editors:
- `neovim.lua`
- `aether.zed.json`

GTK/UI + bars:
- `gtk.css`
- `aether.override.css`
- `steam.css`
- `waybar.css`
- `wofi.css`
- `walker.css`
- `swayosd.css`

WM/lock/notify:
- `hyprland.conf`
- `hyprlock.conf`
- `mako.ini`

System apps:
- `btop.theme`
- `cava_theme`
- `chromium.theme`

## Installation (Placeholder)

To install from a git repo using pipx (recommended):

```bash
pipx install git+https://github.com/OldJobobo/theme-color-tool.git
```

If you do not use pipx, you can also install with pip:

```bash
python3 -m pip install --user git+https://github.com/OldJobobo/theme-color-tool.git
```

Then run from any theme directory (the tool rewrites files in the current folder):

```bash
theme-color-apply -s <Your Base16 Scheme>.yaml
```
