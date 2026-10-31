# Ziro Themes

Community Starship themes for [ziro-shell](https://github.com/Pakrohk/ziro-shell).

## Quick Start

```bash
# Browse themes locally (after cloning this repo)
ls themes/*/

# Apply an official preset
starship preset <name> -o ~/.config/starship.toml
# OR copy directly
cp themes/starship/pastel-powerline.toml ~/.config/starship.toml

# Share your own theme
ziro theme submit
```

## Structure

Themes are organized by contributor namespace:

```
themes/
├── starship/                   ← official Starship presets (curated by ziro)
│   ├── catppuccin-powerline.toml
│   ├── gruvbox-rainbow.toml
│   ├── jetpack.toml
│   ├── pastel-powerline.toml
│   └── tokyo-night.toml
└── <your-github-username>/     ← community contributions
    └── <your-theme-name>.toml
```

> **Note**: Official Starship presets live under `themes/starship/`. These are curated by Ziro for convenience but originate from the [Starship project](https://starship.rs/presets/). Community themes live under `themes/<your-github-username>/`.

## Seeded Presets

| Theme | Origin / Author | Description |
|---|---|---|
| `pastel-powerline` | Starship Project | Soft pastel powerline prompt with powerline arrows |
| `tokyo-night` | Starship Project | Clean dark aesthetic inspired by Tokyo Night |
| `gruvbox-rainbow` | Starship Project | Warm retro gruvbox palette with powerline segments |
| `catppuccin-powerline` | Starship Project | Soothing pastel theme using Catppuccin palette |
| `jetpack` | Starship Project | Modern two-line powerline prompt with rich context |

## Submitting a theme

### Recommended: via `ziro theme submit` (ziro-shell v1.2.4+)

```bash
ziro theme submit
```

This interactive command:
1. Validates that `gh` CLI is installed and authenticated.
2. Checks `~/.config/starship.toml` for customizations.
3. Shows a diff summary of your theme changes.
4. Validates the theme name (kebab-case, 3-30 characters).
5. Creates a branch and opens a Pull Request on this repository automatically.

### Manual Submission

See [CONTRIBUTING.md](CONTRIBUTING.md) for step-by-step instructions for manual fork and PR submission.

## License

[MIT](LICENSE) — same as ziro-shell.
