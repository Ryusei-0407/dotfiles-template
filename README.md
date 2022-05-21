# Template for getting started with dotfiles

> This is for Mac OS users; other operating systems are not covered.
> Be careful not to push your account's private key or password!!

## file structure

- **install.sh** → Script to run the installation
- **Brewfile** → Package to manage the packages to be installed by Homebrew
- **packages** → configuration files under your home directory
- **packages/config** → configuration files under `~/.config`.

Use **GNU Stow** to post links

Ex :

In `stow -v -d ~/dotfiles/packages -t ~ zsh` command in install.sh

Files under packages/zsh will be linked under the home directory.

**packages/zsh/.zshrc** → **~/.zshrc** will be linked to your home directory.

## How to write Brewfile

Ex :

- `brew install git` → `brew "stow"`
- `brew install --cask iterm2` → `cask iterm2`

## Run Install Script!!

```sh
curl -o - https://raw.githubusercontent.com/<UserName>/dotfiles/main/install.sh | sh
```

## Reboot User Machine

```sh
sudo reboot
```

# dotfiles を始めるためのテンプレート

> これは Mac OS ユーザ向けのため、それ以外の OS は対象外です。
> アカウントの秘密鍵やパスワードを push しないように気をつけて下さい!!

## ファイル構成

- **install.sh** → インストールを実行するスクリプト
- **Brewfile** → Homebrew でインストールするパッケージを管理するパッケージ
- **packages** → ホームディレクトリ配下にある設定ファイルを配置する
- **packages/config** → `~/.config` 配下にある設定ファイルを配置する

## リンクを貼る

リンクを貼るのに、**GNU Stow**を使用する

例:

install.sh の `stow -v -d ~/dotfiles/packages -t ~ zsh` のコマンドで

packages/zsh 配下のファイルがホームディレクトリ配下にリンクが貼られる

**packages/zsh/.zshrc** → **~/.zshrc** にリンクが貼られる

## Brewfile の書き方

例:

- `brew install git` → `brew "stow"`
- `brew install --cask iterm2` → `cask iterm2`

## インストールスクリプトの実行

```sh
curl -o - https://raw.githubusercontent.com/<UserName>/dotfiles/main/install.sh | sh
```

## マシンを再起動する

```sh
sudo reboot
```
