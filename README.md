# Zsh-Completions
This repository hosts my collection of Zsh completions for a range of applications I regularly use. I made these due to the absence of pre-existing completions and are shared here because I love Linux and zsh <3
## Installation Instructions
### Quick Start
To activate these completions, prepend the following to your `~/.zshrc` file:
```bash
autoload -Uz compinit && compinit
```
### Setting Permissions
Ensure the completion files are executable:
```bash
chmod 644 _distrobox*
```
### Installation
Completions can be installed in a couple of ways:
#### System-wide:
Copy or symlink the completion files to:
```bash
/usr/share/zsh/functions/Completion/Unix/
```
#### User Custom Directory:
Alternatively, use a custom directory for your completions, such as ~/.local/zsh/completions. If choosing this route, you should add this to your ~/.zshrc:
```bash
    # Custom completion directory
    # set fpath before compinit
    fpath=(~/.local/zsh/completions $fpath)
    autoload -Uz compinit && compinit
```
This method allows for a more portable and organized collection of completions.
### Usage
```bash
user@host $: command<space><tab>
(matching arguments appear with descriptions below prompt)
user@host $: command<space>--[a-z]<tab>(matching arguments appear in line)
```
With the completions installed, Zsh will automatically provide suggestions for commands covered by the completion scripts. This enhances efficiency and reduces the need for memorizing command options.
