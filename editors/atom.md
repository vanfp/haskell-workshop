# Atom

The documentation of Haskell's support in atom is quite good, please follow
instructions on [their website](https://atom-haskell.github.io/installation/).
Make sure you follow the setup for **stack** rather than cabal.

Something to bear in mind is that previous link does not address so well, you'll
need more than one __atom__ package:

- language-haskell -- for syntax highlighting
- ide-haskell -- provides basic capabilities, as well as a backend for other Atom-Haskell packages to use.
- ide-haskell-cabal -- provides a build backend for ide-haskell package based on stack
- ide-haskell-repl -- provides embedded REPL support using infor from ide-haskell-cabal
- haskell-ghc-mod -- opens pipe to _ghc-mod binary_ and queries types, info, typechecks and lints current file.
- autocomplete-haskell -- provides autocompletion using language-haskell and haskell-completion-backend

These __atom__ packages will also need binaries installed by __stack__:

```bash
stack install --install-ghc stylish-haskell ghc-mod
```

The command above will take a while to finish compilation, so better go grab a
coffee or something.
