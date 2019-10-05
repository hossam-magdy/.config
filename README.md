



export RCFILE=$(ls $HOME/.{zsh,bash}rc -a | head -1)
echo 'alias dotfiles="git --git-dir=$HOME/.dotfiles.git/ --work-tree=$HOME"' >> $RCFILE
source $RCFILE
# echo ".dotfiles.git" >> .gitignore
git clone --bare https://www.github.com/username/repo.git $HOME/.dotfiles.git
dotfiles config --local status.showUntrackedFiles no
dotfiles checkout




