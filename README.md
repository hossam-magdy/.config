# config (dotfiles)

This is a [bare](http://www.saintsjd.com/2011/01/what-is-a-bare-git-repository/) git repository for managing [dotfiles](https://wiki.archlinux.org/index.php/Dotfiles)/config in `$HOME` directory.

## Install
```
export RCFILE=$(ls $HOME/.{zsh,bash}rc -a | head -1)
echo 'alias config="git --git-dir=$HOME/.config.git/ --work-tree=$HOME"' >> $RCFILE
source $RCFILE
git clone --bare https://github.com/hossam-magdy/.config $HOME/.config.git
config config --local status.showUntrackedFiles no
config checkout
```

## Usage

git command/alias: `config`

```
config add FILE
config commit -m 'some commit message'
config push
```

## Todo

- Clean `.bashrc`
- Add `macos` branch/config

## Ref

- [Atlassian](https://www.atlassian.com/git/tutorials/dotfiles)
- [archlinux](https://wiki.archlinux.org/index.php/Dotfiles)
- [dotfiles.github.io](https://dotfiles.github.io/)
