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
brew update && brew upgrade 
cd ~
mkdir tmp 
mkdir dev
mkdir incoming

ssh-keygen -t ed25519 -C "email@email.com"

sudo brew install $(< mac-base-packages)
sudo pip install -r python-packages
brew install chezmoi
chezmoi init --apply joroy
``

## Ref (Optional)

```sh
sudo chsh -s /bin/zsh
```
> Reloader la shell

