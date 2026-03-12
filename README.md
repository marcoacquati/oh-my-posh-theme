# oh-my-posh-theme

A custom theme for [Oh My Posh](https://ohmyposh.dev/) — a prompt theme engine for any shell. Designed for a clean, information-dense prompt with a dark-friendly color palette.

---

## Preview

### Prompt layout

```
 ~/projects/my-repo |  main  ↑1 | 󰃩 1 file  1.2s ✓          node 20.11.0
#
```

**Left side** — OS icon · current path · git status · execution time · last command status

**Right side** — Node.js version (with package manager) · Python version (with venv)

**Second line** — prompt character (`#`, highlighted in pink when root)

---

## Color palette

| Name | Hex | Used for |
|---|---|---|
| Mint | `#00BF99` | Path, OS icon, success status |
| Sky Blue | `#149FDF` | Git info |
| Tan (Red) | `#FF4C4C` | Error status, npm icon |
| Pantone Green | `#66CC33` | Node.js |
| PNPM Yellow | `#F9AD00` | pnpm icon |
| Python Yellow | `#FFD43B` | Python |
| Blush | `#CB2A7A` | Root indicator, prompt character |
| White | `#FFFFFF` | Execution time |

---

## Segments

### Left prompt

- **OS icon** — shows the current OS symbol
- **Path** — full path with `/` as separator
- **Git** — upstream icon, branch name, sync status (ahead/behind), working tree changes, staged changes, stash count
- **Execution time** — shows elapsed time for commands that take longer than 500ms
- **Status** — `✓` (mint) on success, `✗` (red) on failure

### Right prompt

- **Node.js** — version, shown only when a relevant config file is present; includes package manager icon (npm / pnpm / yarn)
- **Python** — version and virtualenv name, shown only when a relevant config file is present

### Second line

- `#` prompt character, colored **blush/pink** when running as root, otherwise hidden

---

## Installation

### Prerequisites

Install Oh My Posh by following the [official guide](https://ohmyposh.dev/docs/installation/linux) for your OS.

Make sure you're using a [Nerd Font](https://www.nerdfonts.com/) in your terminal (required for icons to render correctly).

### Apply the theme

Add the following line to your `~/.zshrc`:

```zsh
eval "$(oh-my-posh init zsh --config 'https://raw.githubusercontent.com/marcoacquati/oh-my-posh-theme/main/theme_1.json')"
```

Then reload your shell:

```zsh
source ~/.zshrc
```

### Use locally

If you prefer to keep a local copy:

```zsh
# Download the theme
curl -o ~/.config/oh-my-posh/theme_1.json \
  https://raw.githubusercontent.com/marcoacquati/oh-my-posh-theme/main/theme_1.json

# Point oh-my-posh to the local file
eval "$(oh-my-posh init zsh --config ~/.config/oh-my-posh/theme_1.json)"
```

---

## Requirements

- [Oh My Posh](https://ohmyposh.dev/) v3+
- A [Nerd Font](https://www.nerdfonts.com/) set as your terminal font
- Zsh (or adapt the `init` command for your shell — bash, fish, etc. are also supported)
