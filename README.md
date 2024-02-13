# Zsh-Completions
This repository hosts my collection of Zsh completions for a range of applications I regularly use. First release is distrobox, which I made due to the absence of pre-existing completions and shared here for everyone.
## Installation Instructions
### Quick Start
To activate these completions, prepend the following to your `~/.zshrc` file:
```bash
autoload -Uz compinit && compinit
```
### Setting Permissions
Ensure the completion files are executable:
```bash
chmod 744 _distrobox*
```
### Deployment
Completions can be deployed in a couple of ways:
#### System-wide Placement:
Copy or symlink the completion files to:
```bash
/usr/share/zsh/functions/Completion/Unix/
```
#### Custom Directory:
Alternatively, use a custom directory for your completions, such as ~/.local/zsh/completions. If choosing this route, incorporate the directory into your .zshrc like so:
```bash
    # Custom completion directory
    fpath=(~/.local/zsh/completions $fpath)
    autoload -Uz compinit && compinit
```
This method allows for a more personalized and organized collection of completions.
### Usage
With the completions installed, Zsh will automatically provide suggestions for commands covered by the completion scripts. This enhances efficiency and reduces the need for memorizing command options.
