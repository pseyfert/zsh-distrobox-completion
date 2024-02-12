# zsh-completions
zsh completions including distrobox

This is the initial release of my zsh completions. I intend to generate zsh 
completions for all of the programs I use and publish them here. First release
is distrobox. I didn't find any on github, so I made my own and wanted to share.

Add the following to the top of your ~/.zshrc:

autoload -Uz compinit && compinit

Make sure the files have the proper permissions.

chmod 744 _distrobox*

Place or symlink the files in:

/usr/share/zsh/functions/Completion/Unix/

Or you can use custom completion directory like 
I do such as ~/.local/zsh/completions. If you do this, make sure you add this to
the top of your .zshrc file:

# Custom completion directory

fpath=(~/.local/zsh/completion $fpath)\
autoload -U -z compinit && compinit
