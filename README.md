# dotfiles
Dotfiles for keeping track of configs; deploy with stow symlinks

## Installing stow
`sudo apt install stow`

## Deploying symlinks with Stow
`stow -vt ~ <directory-containing-dotfiles>`

## Deleting deployed symlinks with Stow
`stow -Dvt ~ <directory-containing-dotfiles>`
