# dotfiles

## Installation
Add the **home** alias:

```
alias home="git --work-tree=$HOME --git-dir=$HOME/.home.git"
```

Next, clone the repository to `.home.git` and disable file tracking by default:

```
git clone --bare git@github.com:chmodas/.home.git $HOME/.home.git
home config --local status.showUntrackedFiles no
home checkout
```

That's it. If you encounter any errors such as:

```
error: The following untracked working tree files would be overwritten by checkout:
```

This is because your `$HOME` folder already has files which would be overwritten by Git. The
solution is straightforward: back up the files if you care about them or remove them if you don't.
Once you resolve the issue re-run `home checkout`.
