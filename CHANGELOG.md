# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.0.2] - 2026-06-26

Brings the zsh shell under chezmoi (with Oh My Zsh) and keeps repository metadata
out of `$HOME`.

### Added

- chezmoi-managed zsh config (`dot_zshrc` → `~/.zshrc`) with Oh My Zsh pulled in
  via `.chezmoiexternal.toml`, the `robbyrussell` theme, the `git` plugin, Docker
  Compose aliases, and guarded, `$HOME`-relative tool PATH blocks (Go, NVM,
  PostgreSQL, Android SDK, Yandex Cloud, opencode, LM Studio).
- `user.signingkey` and `[init] defaultBranch = main` in `dot_gitconfig`.
- `.chezmoiignore` excluding repository metadata (`README.md`, `LICENSE`) from
  deployment, so they stay in the repo but never land in `$HOME`.

## [0.0.1] - 2024-12-15

Initial release.

### Added

- `dot_gitconfig` → `~/.gitconfig` — user identity, push/core settings, and
  everyday aliases.
- `dot_vimrc` → `~/.vimrc` — 4-space soft-tab indentation.
- `README.md` and `LICENSE`.

[0.0.2]: https://github.com/memclutter/dotfiles/releases/tag/v0.0.2
[0.0.1]: https://github.com/memclutter/dotfiles/releases/tag/v0.0.1
