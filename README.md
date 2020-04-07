# Shared git config

> Keep your `~/.gitconfig` synchronized across different computers.

## Usage

1. Fork this repo.
1. Run the following on all your computers:

    ```bash
    git clone --depth=1 git@github.com:<your-github-username>/shared-git-config.git ~/shared-git-config
    mv -f ~/.gitconfig ~/shared-git-config/.gitconfig
    ln -s ~/shared-git-config/.gitconfig ~/.gitconfig
    ```

1. When you have modified your git config and you want to publish it everywhere,

    ```bash
    # On the computer where you modified your git config
    cd ~/shared-git-config && git add .gitconfig && git commit && git push`
    # On other computers
    cd ~/shared-git-config && git pull --ff-only
    ```

