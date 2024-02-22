# devbox-setup

## Linux (Ubuntu)

```sh
sudo apt update && sudo apt upgrade 
cd ~
mkdir tmp 
mkdir dev
mkdir incoming

ssh-keygen -t ed25519 -C "email@email.com"

sudo apt install $(< linux-base-packages)
sudo pip install -r python-packages
sudo snap install chezmoi --classic
chezmoi init --apply joroy
```

* GnomeTweaks (Revert Caps/Ctrl)


## MacOS

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
brew update && brew upgrade 
cd ~
mkdir tmp 
mkdir dev
mkdir incoming

brew install gh

# Taf key (default one)
ssh-keygen -t ed25519 -C "joroyw"
ssh-add ~/.ssh/id_ed25519

# Personal key
ssh-keygen -f ~/.ssh/idjoroy -t ed25519 -C "joroy"
ssh-add ~/.ssh/idjoroy


sudo brew install $(< mac-base-packages)
sudo pip install -r python-packages
brew install chezmoi
chezmoi init --apply --ssh joroy
ou (si .ssh/config avec multi-clé https://theboreddev.com/use-multiple-ssh-keys-different-git-accounts/)
chezmoi init --guess-repo-url=false --ssh --apply git@github.com-joroy:joroy/dotfiles.git
``

## Ref (Optional)

```sh
sudo chsh -s /bin/zsh
```
> Reloader la shell

