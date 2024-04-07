# My prompt customization for ZSH shell

This repo is about customizing ZSH shell prompt with my settings.
I'm using a macbook air M2, so I use the battery indicator, and Wifi connexion.

## macOS

### Requirements

Mandatory:
- ZSH shell
- Oh My ZSH: https://ohmyz.sh/#install
- A custom font: https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#manual-font-installation
  I use the recommanded one: MesloLGS NF
- Powerlevel10k: https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#oh-my-zsh

Optional but recommended
- I use iTerm2, but I think all terminal should works, but it must be able to use a custom font
- Homebrew:  https://brew.sh
- Archey4: https://github.com/HorlogeSkynet/archey4
- eza binary: https://formulae.brew.sh/formula/eza
- OMZ plugins I use: 
  - zsh-syntax-highlighting: https://github.com/zsh-users/zsh-syntax-highlighting
  - zsh-autosuggestions: https://github.com/zsh-users/zsh-autosuggestions
  - zsh-completions: https://github.com/zsh-users/zsh-completions
  - zsh-eza: https://github.com/z-shell/zsh-eza?tab=readme-ov-file#with-oh-my-zsh + 
      - need eza binary installed
  - eza : https://github.com/eza-community/eza/blob/main/INSTALL.md#completions

### The `.zshrc` file

Edit my .zshrc file, available in the repository, and see what' inside.

Chnage your `YOUR_NAME` with your name/pseudo :
```zsh
prompt_my_name()  {
  p10k segment -b blue -f white -t 'YOUR_NAME' -i '🎲'
  # p10k segment -b blue -f darkblue -t "$(whoami)🌀$(hostname)" -i '🤖'
}
```

Here the `plugins` line I use:
```zsh
plugins=(iterm2 git macos zsh-autosuggestions zsh-syntax-highlighting zsh-completions colored-man-pages brew z aliases command-not-found sudo docker python virtualenv colorize zsh-eza)
```
You need to remove any unnecessary plugins. For example, if you don't use docker, remove `docker` plugin.

I also use some functions to show and define aliases for some commands. Feel free to change them.
All improvements are welcome, so submit you Pull requests.

### For Windows

I use Windows Terminal, but as for macOS, you should use any terminal that can use a custom font.

⚠️🚨 Work in progress 🚨⚠️