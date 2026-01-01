# Repository Guidelines

## Project Structure & Module Organization
- `theme_color_tool/` contains the installable Python package; `apply_theme.py` holds the main logic.
- `apply-theme.py` is a small CLI entrypoint that forwards args to the package.
- `README.md` documents usage; `pyproject.toml` defines packaging metadata and the `theme-color-apply` console script.

## Build, Test, and Development Commands
- `python3 apply-theme.py -s path/to/scheme.yaml` runs the tool against the current theme directory.
- `python3 -m theme_color_tool.apply_theme -s path/to/scheme.yaml` runs the module directly.
- `theme-color-apply -s path/to/scheme.yaml` runs the installed console script after packaging.
- `pipx install git+https://...` installs the tool for local use (see `README.md` for the placeholder).

## Coding Style & Naming Conventions
- Use 4-space indentation and standard Python conventions (PEP 8).
- Prefer `snake_case` for functions/variables and `UPPER_SNAKE_CASE` for constants.
- Keep regexes and file updates localized in `theme_color_tool/apply_theme.py` to avoid scattered logic.
- No formatter or linter is configured; keep diffs minimal and consistent with existing style.

## Testing Guidelines
- No automated tests are present yet. If you add tests, place them under a `tests/` directory and name files `test_*.py`.
- When changing a file updater, manually verify against a representative theme file (e.g., `kitty.conf`, `waybar.css`).

## Commit & Pull Request Guidelines
- No Git history is available in this checkout. Use concise, imperative subjects (e.g., “Add Zed theme mapping”).
- Include a brief PR description of the affected theme files and a sample scheme used for verification.

## Configuration Notes
- The tool expects to run inside a theme repository and rewrites supported files in place.
- Base16 scheme files must provide `base00`-`base0F` keys (hex colors).
