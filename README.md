# Omarchy Theme Apply Tool

Applies a Base16 YAML scheme to the theme files in the current directory.

This script is intended to be run from inside an Omarchy theme repo.
It rewrites each supported file with the color values from the scheme.

## Usage

```bash
python3 apply-theme.py -s base16-scheme.yaml  # example scheme file
```

## Options

- `-s`, `--scheme` Path to a Base16 YAML scheme file.
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
pipx install git+https://github.com/yourname/omarchy-theme-tool
```

If you do not use pipx, you can also install with pip:

```bash
python3 -m pip install --user git+https://github.com/yourname/omarchy-theme-tool
```

Then run from any theme directory (the tool rewrites files in the current folder):

```bash
omarchy-apply -s base16-scheme.yaml  # example scheme file
```
