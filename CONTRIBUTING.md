# Contributing Themes to Ziro Themes

Thank you for contributing your theme to the Ziro community!

## Guidelines

1. **Format**: Themes must be valid Starship TOML configuration files (`.toml`).
2. **Naming**:
   - Theme names must use lowercase `kebab-case` (`^[a-z0-9][a-z0-9-]{1,28}[a-z0-9]$`).
   - Length: 3 to 30 characters.
   - Example: `my-neon-flow.toml`.
3. **No Secrets**: Never include private API keys, cloud tokens, database URLs, or personal passwords in your configuration.
4. **Location**: Place your theme file under `themes/<your-github-username>/<theme-name>.toml`.

---

## Submission Methods

### 1. Automated Submission (Recommended)

From `ziro-shell` (v1.2.4+):

```bash
ziro theme submit
```

Options:
- `--name <name>`: Specify theme name directly.
- `--dry-run`: Preview changes without opening a PR.
- `--no-pr`: Push branch without opening a PR.

### 2. Manual Submission via GitHub

1. Fork this repository: [Pakrohk/ziro-themes](https://github.com/Pakrohk/ziro-themes).
2. Clone your fork locally:
   ```bash
   git clone https://github.com/<your-username>/ziro-themes.git
   cd ziro-themes
   ```
3. Create a feature branch:
   ```bash
   git checkout -b submit/<your-username>/<theme-name>
   ```
4. Create your user directory and add your theme:
   ```bash
   mkdir -p themes/<your-username>
   cp ~/.config/starship.toml themes/<your-username>/<theme-name>.toml
   ```
5. Commit and push:
   ```bash
   git add themes/<your-username>/<theme-name>.toml
   git commit -m "feat(themes): add <theme-name> by @<your-username>"
   git push -u origin submit/<your-username>/<theme-name>
   ```
6. Open a Pull Request against `main` on `Pakrohk/ziro-themes`.
