## zsh
```sh
sudo apt install zsh
sudo chsh -s $(which zsh)
```
## nvm
```sh
# Get the latest version of NVM
NVM_VERSION=$(curl -s "https://api.github.com/repos/nvm-sh/nvm/releases/latest" | grep -Po '"tag_name": "v\K[^"]*')

# Use the version in the curl command
curl -o- "https://raw.githubusercontent.com/nvm-sh/nvm/v$NVM_VERSION/install.sh" | bash

# ~./zshrc
export NVM_DIR=~/.nvm
[ -s "$NVM_DIR/nvm.sh ] && / "$NVM_DIR/nvm.sh"
```
## zsh-autosuggestions
```sh
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
# Add next line to .zshrc
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
## [warp](https://www.warp.dev/)
Get themes from [kedarmd/warp-themes](https://github.com/kedarmd/warp-themes)
Download the `.yml` file and run following command
```sh
mv ~/Downloads/{{filename}}.yml ~/.local/share/warp-terminal/themes/
```
## postman
## vscode

