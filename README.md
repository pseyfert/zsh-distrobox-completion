# zsh-completions
zsh completions including distrobox

This is the initial release of my zsh completions. I intend to generate zsh completions for all of the programs I use and publish them here. First release is distrobox. I didn't find any on github, so I made my own and wanted to share. Place the distrobox directory and its contents in /usr/share/zsh/functions/Completion/Unix/ or a custom completion directory like I do such as ~/.local/zsh/completions. If you do this, make sure you add this to the top of your .zshrc file:

# for a custom zsh completion directory

fpath+=(~/.local/zsh/completion $fpath)\
autoload -U -z compinit && compinit
