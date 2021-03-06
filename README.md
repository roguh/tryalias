# tryalias

`tryalias openpdf "zathura --fork" evince mupdf-x11 mupdf openoffice gimp reader10.exe`

Aliases with fallbacks.

The `tryalias` command works like `alias`, but it sequentially checks
each of its multiple arguments until it finds a valid command.
If no argument is found, alias the first argument to the last argument.

## Installation

### fish

Place your tryalias commands in `~/.aliases`.
Copy `tryalias.fish` to `~/.config/fish/functions/` and source `~/.aliases`
in your `config.fish`. See `config.fish-sample`.

### bash or zsh

Place your tryalias commands in `~/.aliases`.

```
$ cp .tryalias ~
$ cat bashrc-sample >> ~/.bashrc
```

### csh

Place your tryalias commands in `~/.aliases`.

In csh, `tryalias` is an alias for `alias`.
See `cshrc-sample`.

## Usage

```
tryalias please sudo

# Use previously defined aliases
tryalias exa "exa --git"
tryalias l "exa -Fa" "ls -Fa"
tryalias ll "l -lh"

# Confirm overwrites and deletions
tryalias mv "mv -i"
tryalias cp "cp -i"
tryalias rm "rm -i"

# PDF reader
tryalias e "zathura --fork" evince mupdf-x11 mupdf 

# Favorite editor?
tryalias v vis nvim vim vi elvis ex-vi nano ed gedit libreoffice openoffice "playonlinux --run 'Microsoft Powerpoint 2010'"

# Start emacs with CLI 
tryalias em "emacs -nw"

# Start emacs client. Start daemon if its not running.
tryalias emc "emacsclient -nw --alternate-editor="""
```
