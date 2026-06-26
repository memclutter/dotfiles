# Dotfiles

[![Latest release](https://img.shields.io/github/v/release/memclutter/dotfiles?sort=semver)](https://github.com/memclutter/dotfiles/releases/latest)
[![License: MIT](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![Managed with chezmoi](https://img.shields.io/badge/managed%20with-chezmoi-blue)](https://chezmoi.io)

My personal dotfiles, managed with [chezmoi](https://chezmoi.io) so a single
`chezmoi apply` brings a fresh machine up to my development setup.

## What's included

- **Git** (`~/.gitconfig`) — identity, signing key, `init.defaultBranch = main`,
  push/core settings, and everyday aliases.
- **Vim** (`~/.vimrc`) — 4-space soft-tab indentation.
- **Zsh** (`~/.zshrc`) — [Oh My Zsh](https://ohmyz.sh) (cloned automatically by
  chezmoi), the `robbyrussell` theme, the `git` plugin, Docker Compose aliases,
  and guarded tool PATH blocks (Go, NVM, PostgreSQL, Android SDK, Yandex Cloud,
  opencode, LM Studio) that skip cleanly when a tool isn't installed.

## Usage

Install [chezmoi](https://chezmoi.io/install/), then initialise from this repo
and apply:

```sh
chezmoi init --apply memclutter
```

To pull and apply later updates:

```sh
chezmoi update
```

On first apply, Oh My Zsh is cloned to `~/.oh-my-zsh` via
[`.chezmoiexternal.toml`](.chezmoiexternal.toml); the framework keeps itself up
to date afterwards.

## Notes

- Repository metadata (`README.md`, `LICENSE`, `CHANGELOG.md`) is listed in
  [`.chezmoiignore`](.chezmoiignore), so it stays in the repo but is never
  deployed to `$HOME`.
- See [CHANGELOG.md](CHANGELOG.md) for release history.

Feel free to fork and adapt these to your own preferences. Happy coding!

## License

[MIT](LICENSE)
