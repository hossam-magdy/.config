# dotfiles

## Install
```
export RCFILE=$(ls $HOME/.{zsh,bash}rc -a | head -1)
echo 'alias dotfiles="git --git-dir=$HOME/.dotfiles.git/ --work-tree=$HOME"' >> $RCFILE
source $RCFILE
git clone --bare https://github.com/hossam-magdy/.dotfiles $HOME/.dotfiles.git
dotfiles config --local status.showUntrackedFiles no
dotfiles checkout
```

## Usage

git command/alias: `dotfiles`

`dotfiles add FILE`

`dotfiles commit -m 'some commit message'`

`dotfiles push`
