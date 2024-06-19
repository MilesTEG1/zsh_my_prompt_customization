# My prompt customization for ZSH shell

This repo is about customizing ZSH shell prompt with my settings.
I'm using a MacBook Air M2, so I use the battery indicator, and Wifi connexion.
I also remote control some linux environment like Proxmox, VM, LXC...

## Shared requirements

### Mandatory:
- ZSH shell
- Oh My ZSH: https://ohmyz.sh/#install
- A custom font: https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#manual-font-installation
  I use the recommanded one: [FiraCode NerdFont](https://www.programmingfonts.org/#firacode), or MesloLG NerdFont
  To get the latest version of Nerd Font, go here : [https://www.nerdfonts.com/font-downloads](https://www.nerdfonts.com/font-downloads)
- Powerlevel10k: https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#oh-my-zsh

### For macOS

Optional but recommended
- I use iTerm2, but I think all terminal should works, but it must be able to use a custom font
- Homebrew:  https://brew.sh
- Archey4: https://github.com/HorlogeSkynet/archey4
- eza binary: https://github.com/eza-community/eza
- OMZ plugins I use: 
  - zsh-syntax-highlighting: https://github.com/zsh-users/zsh-syntax-highlighting
  - zsh-autosuggestions: https://github.com/zsh-users/zsh-autosuggestions
  - zsh-completions: https://github.com/zsh-users/zsh-completions
  - zsh-eza: https://github.com/z-shell/zsh-eza?tab=readme-ov-file#with-oh-my-zsh + 
      - need eza binary installed
  - eza : https://github.com/eza-community/eza/blob/main/INSTALL.md#completions

### For Linux

> [!IMPORTANT] 
> I don't use directly a Linux Terminal, I always do remote control from my mac with iTerm2, or with Proxmox Console WebUI.

- I use iTerm2 to remote control, but I think all terminal should works, but it must be able to use a custom font
- neofetch: https://github.com/dylanaraps/neofetch
  By seraching for this link, I just found that this project is now archived... I'll check some alternative someday : https://itsfoss.com/neofetch-alternatives/
- eza binary: https://formulae.brew.sh/formula/eza
- OMZ plugins I use: 
  - zsh-syntax-highlighting: https://github.com/zsh-users/zsh-syntax-highlighting
  - zsh-autosuggestions: https://github.com/zsh-users/zsh-autosuggestions
  - zsh-completions: https://github.com/zsh-users/zsh-completions
  - zsh-eza: https://github.com/z-shell/zsh-eza?tab=readme-ov-file#with-oh-my-zsh + 
      - need eza binary installed
  - eza : https://github.com/eza-community/eza/blob/main/INSTALL.md#completions


### For Windows

I use Windows Terminal, but as for macOS, you should use any terminal that can use a custom font.

⚠️🚨 Work in progress 🚨⚠️

---

## The `.zshrc` file

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

## Some screenshots

### Remote control of PVE terminal

![alt text](https://github.com/MilesTEG1/zsh_my_prompt_customization/blob/0a6c658684164c14a3f34cebef05ecd14fa37cec/Linux-Proxmox/screenshot_iTerm2.png?raw=true)

### My macOS terminal

![alt text](https://github.com/MilesTEG1/zsh_my_prompt_customization/blob/main/macOS_iTerm2/screenshot_iTerm2.png?raw=true)