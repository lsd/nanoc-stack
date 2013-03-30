MacVim / vim config
 http://github.com/lsd/vim
 Updated 01/26/2013
 Note This is WORK IN PROGRESS
===
~/.vimrc and ~/.vim directories. I use MacVim but this setup should be OS-agnostic.
Extraneous buffers are enabled in MacVim but not console vim, for which toggle keys 
exist to open up NERDTree, Taglist, MiniBuffexplorer, etc.

DEPENDENCIES
===
This config uses (and includes) NeoBundle for plugin management.
For manual installation, remove bundle/neobundle.vim
from the repo and follow the instructions on
https://github.com/Shougo/neobundle.vim

SCREENSHOT
===
![Alt text](https://raw.github.com/lsd/vim/master/screenshot-mac.png "MacVim 7.3 colorscheme wombat on 10.8.2 with Inconsolata:18")

INSTALLATION
===
Clone repo, symlink ~/.vimrc to repo/vimrc and ~/.vim to repo

Install the Inconsolata font in the fonts dir or remove the guifont line

Launch MacVim or vim and run :NeoBundleInstall to install the plugins

CONSOLE VIM?
===
I disable the left/right sidebars when opening vim in a console. They only auto
open in MacVim because of how I use MacVim and vim. If you want these buffers
to open with vim, remove the if has("gui_running") clause
## Lightweight stack for rapid development 
## of (mostly) static sites.
### github.com/lsd

To install and start, type:
$ bundle install
$ foreman start

Review Rules, nanoc.yml and Procfile
Access the site at http://localhost:5000


----------

STRUCTURE

A site has the following files and directories:
  nanoc.yaml contains the site configuration
  Rules contains compilation, routing and layouting rules
  content/ contains the uncompiled items
  layouts/ contains the layouts
  lib/ contains custom site-specific code (filters, helpers, …)
  output/ contains the compiled site
  tmp/ For speeding up compilation (can be safely emptied)


NOTES: lib/ dir
will load all Ruby files in lib before it starts compiling. 
All method definitions, class definitions, available during 
compilation process. This dir is quite useful for putting 
in site-wide helpers, filters, data sources, etc.


