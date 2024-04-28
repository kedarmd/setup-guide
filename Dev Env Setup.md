## zsh
```sh
sudo apt install zsh
```
## nvm
```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
# ~./zshrc
export NVM_DIR=~/.nvm
[ -s "$NVM_DIR/nvm.sh ] && / "$NVM_DIR/nvm.sh"
```
## nvim with ([kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim))
```sh
git clone https://github.com/kedarmd/kickstart.nvim.git "${XDG_CONFIG_HOME:-$HOME/.config}"/nvim
```
* Use the latest version of Neovim
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
## [warp](https://www.warp.dev/)
Get themes from [kedarmd/warp-themes](https://github.com/kedarmd/warp-themes)
Download the `.yml` file and run following command
```sh
mv ~/Downloads/{{filename}}.yml ~/.local/share/warp-terminal/themes/
```
## postman
## vscode

