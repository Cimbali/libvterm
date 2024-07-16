# Libvterm mirrors

This repo stores various mirrors of libvterm in different branches, automatically updated. [![Update mirrors](https://github.com/Cimbali/libvterm/actions/workflows/update.yml/badge.svg)](https://github.com/Cimbali/libvterm/actions/workflows/update.yml)

- [bazaar](https://github.com/Cimbali/libvterm/tree/bazaar): mirrors [original (or upstream) code repo](https://bazaar.leonerd.org.uk/c/libvterm/).
  This is done with [breezy](https://www.breezy-vcs.org/doc/en/) fast-export and git fast-import for consistent results.

  Numbered revisions are available under the `refs/bazaar-revision/*`, e.g. [rev 789](https://github.com/Cimbali/libvterm/tree/refs/bazaar-revision/789)
- [vim](https://github.com/Cimbali/libvterm/tree/vim): mirrors the [`src/libvterm/` subdirectory of vim](https://github.com/vim/vim/tree/master/src/libvterm)
  This is extracted using git subtree command, and artificially “grafted” onto a bazaar commit to provide common history.
  The selected common ancestor is the commit that seemed most appropriate (smallest diff), but may be historically incorrect.
- [nvim](https://github.com/Cimbali/libvterm/tree/nvim): mirrors [the neovim fork of libvterm](https://github.com/neovim/libvterm).

This allows to compare the branches (with https://github.com/Cimbali/libvterm/compare/rev1...rev2) to see what divergences happened since forking. For example:
- [changes in upstream since rev 789](https://github.com/Cimbali/libvterm/compare/bazaar-revision/789...bazaar)
- [divergence in vim since forking](https://github.com/Cimbali/libvterm/compare/bazaar...vim)
- [changes in bazaar reflow branch](https://github.com/Cimbali/libvterm/compare/bazaar...bazaar-reflow)
