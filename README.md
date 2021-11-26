# Libvterm mirrors

This repo stores various mirrors of libvterm in different branches, automatically updated.

- bazaar: mirrors original code, http://bazaar.leonerd.org.uk/c/libvterm/
  This is done with [breezy](https://www.breezy-vcs.org/doc/en/) fast-export and git fast-import for consistent results.
- vim: mirrors the src/libvterm/ subdirectory of https://github.com/vim/vim
  This is extracted using git subtree command, and artificially “grafted” onto a bazaar commit to provide common history.
  The selected common ancestor is the commit that seemed most appropriate (smallest diff), but may be historically incorrect.
- nvim: mirrors https://github.com/neovim/libvterm
  This seems to be a truncated version of the bazaar branch, until some release (v0.1.3 at time of writing),
  with commits sha1s inconsistent with the version of importing bazaar commits used in the repo.
