# dotfiles

## Installation
Add the **home** alias:

```
alias home="git --work-tree=$HOME --git-dir=$HOME/.home.git"
```

Next, clone the repository to `.home.git` and disable file tracking by default:

```
git clone git@github.com:chmodas/.home.git $HOME/.home.git
home config --local status.showUntrackedFiles no
```

That's it.
