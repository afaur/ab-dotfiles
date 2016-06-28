# Browser dotfiles

## Install

1. Clone the base dotfiles

  ~~~
  git clone git://github.com/blainesch/ab-dotfiles.git ~/dotfiles
  ~~~

1. Clone your personal dotfiles to `~/dotfiles-local`
1. Install [rcm](https://github.com/thoughtbot/rcm):

  ~~~
  brew tap thoughtbot/formulae
  brew install rcm
  ~~~

1. Install the dotfiles:

  ~~~
  env RCRC=$HOME/dotfiles/rcrc rcup
  ~~~

1. Optionally, you can safely run `rcup` multiple times to update:

  ~~~
  rcup
  ~~~

## Extending

The command `rcup` does more than just copy a few dotfiles it has support for
`hooks` and `bin` files.

Read more about
[rcm](https://robots.thoughtbot.com/rcm-for-rc-files-in-dotfiles-repos)

### Hooks

For example you could create a `hooks/post-up` to install your vim package
manager, or do some host specific configuration.

### Bin

If you have a binary such as `bin/foo` it'll add that command to your path.
Ensure these files have execute permission.

### Defaults

By default this will look for:

* `~/.gitconfig.local`
* `~/.tmux.conf.local`
* `~/.vimrc.local`
* `~/.vimrc.bundles.local`
