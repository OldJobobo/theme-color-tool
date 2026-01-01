# Theme Color Tool

Apply a Base16 YAML scheme to theme files in the current directory. This tool is
meant to run inside a theme repo and rewrites supported files in place using the
Base16 `base00`-`base0F` values.

## Installation

Install with pipx (recommended):

```bash
pipx install git+https://github.com/OldJobobo/theme-color-tool.git
```

Or install with pip:

```bash
python3 -m pip install --user git+https://github.com/OldJobobo/theme-color-tool.git
```

## Usage

Installed (from any theme directory):

```bash
theme-color-apply -s <Your Base16 Scheme>.yaml
```

From the repo without installing:

```bash
python3 apply-theme.py -s <Your Base16 Scheme>.yaml
```

Module form:

```bash
python3 -m theme_color_tool.apply_theme -s <Your Base16 Scheme>.yaml
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
