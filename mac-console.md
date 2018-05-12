# Mac console environment configuration

## Vim colorization

Create `~/.vimrc` and put:

```bash
filetype plugin indent on
syntax on
```

## Bash colorization

Create `~/.bash_profile` if not exists and put:

```bash
export PS1="\[\033[36m\]\u\[\033[m\]@\[\033[32m\]\h:\[\033[33;1m\]\w\[\033[m\]\$ "
export CLICOLOR=1
export LSCOLORS=ExFxBxDxCxegedabagacad
alias ls='ls -GFh'
```

The first line changes the bash prompt to be colorized, and rearranges the prompt to be `username@hostname:cwd $`.

The next two lines enable command line colors, and define colors for the `ls` command

Finally, we alias `ls` to include a few flags by default. `-G` colorizes output, `-h` makes sizes human readable, and `-F` throws a `/` after a directory, `*` after an executable, and a `@` after a symlink, making it easier to quickly identify things in directory listings.
