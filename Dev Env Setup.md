## zsh
```sh
sudo apt install zsh
chsh -s $(which zsh)
```
## nvm
```sh
# Get the latest version of NVM
NVM_VERSION=$(curl -s "https://api.github.com/repos/nvm-sh/nvm/releases/latest" | grep -Po '"tag_name": "v\K[^"]*')

# Use the version in the curl command
curl -o- "https://raw.githubusercontent.com/nvm-sh/nvm/v$NVM_VERSION/install.sh" | bash

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion

# install latest LTS version
nvm install --lts
```
## git
```sh
sudo apt install git
git config --global user.name "kedarmd"
git config --global user.email "dindekedar@gmail.com"
```
## github ssh
```sh
ssh-keygen -t ed25519 -C "dindekedar@gmail.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
# to get ssh key
cat ~/.ssh/id_ed25519.pub
```

## zsh-autosuggestions
```sh
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
# Add next line to .zshrc
echo 'source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh' >> ~/.zshrc
```
## [lazygit](https://github.com/jesseduffield/lazygit)
```sh
LAZYGIT_VERSION=$(curl -s "https://api.github.com/repos/jesseduffield/lazygit/releases/latest" | grep -Po '"tag_name": "v\K[^"]*')
curl -Lo lazygit.tar.gz "https://github.com/jesseduffield/lazygit/releases/latest/download/lazygit_${LAZYGIT_VERSION}_Linux_x86_64.tar.gz"
tar xf lazygit.tar.gz lazygit
sudo install lazygit /usr/local/bin
```
## [starship](https://starship.rs/installing/)/oh-my-zsh
```sh
curl -sS https://starship.rs/install.sh | sh
# ~/.zshrc
eval "$(starship init zsh)"
```
* create a file named `starship.toml` to configure the theme and place it in `~/.config`

## WezTerm
```sh
curl -fsSL https://apt.fury.io/wez/gpg.key | sudo gpg --yes --dearmor -o /usr/share/keyrings/wezterm-fury.gpg
echo 'deb [signed-by=/usr/share/keyrings/wezterm-fury.gpg] https://apt.fury.io/wez/ * *' | sudo tee /etc/apt/sources.list.d/wezterm.list
sudo apt update
sudo apt install wezterm
```
Now install [nvim-wez-navigator](https://github.com/kedarmd/nvim-wez-navigator) for better Neovim-WezTerm Navigation
```sh
git clone https://github.com/kedarmd/nvim-wez-navigator.git ~/.config/wezterm/plugins/nvim-wez-navigator/
```
## Nerd Font
```sh
wget "https://github.com/ryanoasis/nerd-fonts/releases/download/v$(curl -s "https://api.github.com/repos/ryanoasis/nerd-fonts/releases/latest" | grep -Po '"tag_name": "v\K[^"]*')/JetBrainsMono.zip"
unzip JetBrainsMono.zip -d ~/Downloads/JetBrainsMono
find ~/Downloads/JetBrainsMono -type f -name "*JetBrainsMonoNerdFontMono-Regular.ttf" -exec bash -c 'mkdir -p ~/.local/share/fonts && mv "$1" ~/.local/share/fonts/' bash {} \;
rm -rf ~/Downloads/JetBrainsMono
rm -r ~/JetBrainsMono.zip
fc-cache -fv
```

## TMUX
```sh
sudo apt install tmux
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
tmux source ~/.tmux.conf
```

## Neovim & required dependencies
```sh
sudo snap install nvim --classic
sudo apt install make gcc ripgrep unzip xclip xsel
```

## Deno
```sh
curl -fsSL https://deno.land/install.sh | sudo DENO_INSTALL=/usr/local sh
```

## postman
## vscode

