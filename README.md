# Libvterm mirrors

This repo stores various mirrors of libvterm in different branches, automatically updated. [![Update mirrors](https://github.com/Cimbali/libvterm/actions/workflows/update.yml/badge.svg)](https://github.com/Cimbali/libvterm/actions/workflows/update.yml)

- [bazaar](https://github.com/Cimbali/libvterm/tree/bazaar): mirrors [original (or upstream) code repo](http://bazaar.leonerd.org.uk/c/libvterm/).
  This is done with [breezy](https://www.breezy-vcs.org/doc/en/) fast-export and git fast-import for consistent results.
- [vim](https://github.com/Cimbali/libvterm/tree/vim): mirrors the [`src/libvterm/` subdirectory of vim](https://github.com/vim/vim/tree/master/src/libvterm)
  This is extracted using git subtree command, and artificially “grafted” onto a bazaar commit to provide common history.
  The selected common ancestor is the commit that seemed most appropriate (smallest diff), but may be historically incorrect.
- [nvim](https://github.com/Cimbali/libvterm/tree/nvim): mirrors [the neovim fork of libvterm](https://github.com/neovim/libvterm)
  This seems to be a truncated version of the bazaar branch, until some release (v0.1.3 at time of writing).

This allows to e.g. [compare the branches](https://github.com/Cimbali/libvterm/compare/vim...bazaar) to see what divergences happened since forking.
