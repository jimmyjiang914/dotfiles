# dotfiles
Dotfiles for keeping track of configs; deploy with stow symlinks

## Installing stow
- macOS: `brew install stow`
- Debian/Ubuntu: `sudo apt install stow`

## Deploying symlinks with Stow
`stow -vt ~ --no-folding <directory-containing-dotfiles>`

`--no-folding` makes stow link individual files instead of whole directories.
Without it, on a fresh machine where `~/.config` doesn't exist yet, stow would
symlink all of `~/.config` into this repo, and other apps' configs would land here.

## Deleting deployed symlinks with Stow
`stow -Dvt ~ <directory-containing-dotfiles>`

## Machine-local files (not tracked)
- `~/.config/git/user`: git identity, included by `git/.config/git/config`
  ```ini
  [user]
          name = Your Name
          email = you@example.com
  ```
