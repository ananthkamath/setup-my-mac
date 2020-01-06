# Setup-My-Mac

Setup-my-mac will setup your Macbook from scratch

## How to install

```
curl -fsSL https://raw.githubusercontent.com/ananthkamath/setup-my-mac/master/start | ruby
```
The above command will prompt for installing xcode-select, after that installs, enter the password and continue with the script.
This script will clone the setup-my-mac repo into `/tmp/setup-my-mac` and then run it for you.

## Troubleshooting

1. Ansible fails due to errors relating to sudo/password or any other error:

Rerun the script with the following command(-K is for `--ask-become-pass`):
```
cd /tmp/setup-my-mac
ansible-playbook -K setup.yml
```

2. Ansible fails because some utility/software was already installed:

  Make sure that you don't have anything pre-installed when running setup-my-mac.
  If you need to install something please ensure brew was used to install it or else the script will fail.

  If you did install something without homebrew, then please delete the software's name from the file, `setup.yml` and rerun the script.

## What it installs

### Terminal Utilities
- vim
- git
- fzf
- the_silver_searcher
- zsh
- z
- OhMyZsh
- rbenv
- tfenv
- node

### Applications
- Docker Edge
- Firefox Developer Edition
- Iterm2
- Postman
- Slack
- Spotify
- Sublime Text 3
- Vscode

## After installation
- Setup ssh
- Make changes to the gitconfig added
