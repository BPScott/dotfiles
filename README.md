# Dotfiles

These are my dotfiles. There are many like them, but these are mine.

This is a rough first draft, structure and bootstrapping shall come
with time.

## Getting Started

### OSX

Install XCode & XCode Developer Tools then run the following:

    # Install [HomeBrew](http://mxcl.github.com/homebrew/)
    ruby -e "$(curl -fsSkL raw.github.com/mxcl/homebrew/go)"
    # Install vim from homebrew
    brew install vim
    # Clone this repository
    git clone https://github.com/BPScott/dotfiles.git ~/dotfiles
    # Run the setup script to generate common symlinks
    cd ~/dotfiles && rake
    # Link Sublime Config as is OS specific
    ln -s ~/dotfiles/sublime ~/Library/Application\ Support/Sublime\ Text\ 2/Packages/User
    # Make zsh the default shell
    chsh -s /bin/zsh
    # Close and restart your terminal

### Ubuntu

    # Install zsh, git and vim
    sudo apt-get install zsh git-core vim
    # Clone this repository
    git clone https://github.com/BPScott/dotfiles.git ~/dotfiles
    # Run the setup script to generate common symlinks
    cd ~/dotfiles && rake
    # Link Sublime Config as is OS specific
    ln -s ~/dotfiles/sublime ~/.config/sublime-text-2/Packages/User
    # Make zsh the default shell
    chsh -s /bin/zsh
    # Close and restart your terminal

## Going Further

### OSX

* Import misc/colorschemes/monokai.itermcolors into iTerm2

### Ubuntu

* Copy XFCE-Terminal color config into its location

        cp misc/colorschemes/terminalrc ~/.config/Terminal/terminalrc

## Inspiration / Blatant Copying

[AndrewVos](https://github.com/AndrewVos/vimfiles)
[Cowboy](https://github.com/cowboy/dotfiles)
[Holman](https://github.com/holman/dotfiles)
[Sorin-Ionescu](https://github.com/sorin-ionescu/dot-files)

