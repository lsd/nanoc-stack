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


