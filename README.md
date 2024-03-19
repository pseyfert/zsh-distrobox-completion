# Zsh-Completions
This repository hosts my collection of zsh completions for a range of applications I regularly use. I made these due to the absence of pre-existing completions and are shared here because I love Linux and zsh <3
## Installation Instructions
### Quick Start
To activate these completions, put this in your `~/.zshrc` file:
```bash
autoload -Uz compinit && compinit
```
### Setting Permissions
Perform this on all completion files:
```bash
chmod 644 _distrobox*
```
### Installation
Completions can be installed in a couple of ways.
#### System-wide:
Copy or symlink the completion files to:
```bash
/usr/share/zsh/site-functions
# or
/usr/local/share/zsh/site-functions
# or one of the folders listed by running
echo $fpath
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
### Usage Example
This section demonstrates how to use the zsh completions from this collection. zsh completions enhance your command-line experience by providing arguments, options and subcommands suggestions as you type, making it easier and faster to construct commands.
#### Invoking Completions
1. **Initial Command Entry**
    Begin by typing your command in the terminal. After the command, add a space to indicate you're ready to enter arguments or options.
    ```zsh
    user@host $: command<space>
    ```
2. **Activating Argument Suggestions**
    After typing the command and a space, press `<Tab>` to trigger the zsh completion system. This will display matching arguments along with their descriptions below the prompt, making it easier to understand what each argument does.

    Example output after pressing `<Tab>`:
    ```
    user@host $: command<space>
    --option1  Description for option1
    --option2  Description for option2
    ...
    ```
    This helps you quickly find the argument you need without memorizing every option.
3. **Activating Inline Argument Suggestions**
    For a more streamlined experience, you can start typing an option with its leading dashes `-` or `--` followed by any letter from `a-z`, and then press `<Tab>` to filter arguments inline.
    ```zsh
    user@host $: command<space>--[a-z]<Tab>
    ```
    This method displays matching arguments directly in line with your current command, allowing for a quick selection of the desired option without cluttering the terminal with descriptions.

    Example after typing `--a` and pressing `<Tab>`:
    ```
    user@host $: command --argument1
    ```
    The inline suggestions are particularly useful for quickly completing longer option names or when you are familiar with the options but need a quick reminder of the exact syntax.

With completions installed and compinit enabled, zsh will automatically provide suggestions for commands covered by the completion scripts.
