# Hi, nerd.

This page intentionally leaves out graphs, badges, and personality quizzes.
If you were looking for flair, it was redirected:
```bash
# contribution graphs, last seen here:
git log --since=1970 | awk '{print $1}' | wc -l > /dev/null
# sorry, I piped them to /dev/null to save disk space.
```

I prefer [reproducible things](https://github.com/inverted-tree/nixos-config/). Everything else is incidental.
```nix
{ config, ... }@args:
let
  inherit (args) inputs;
in {
  imports = [ ../github-profile.nix ];

  environment.variables.EDITOR = "nvim"

  environment.systemPackages = with config; [
    dotfiles
    nixos
  ];
  
  system.stateVersion = "25.11";
}
```

Minimal description, maximum signal.
```haskell
module Profile where

type Determinism = Bool
type Taste = String

data Tooling = Vim | NixOS | Ninja deriving (Eq, Show)
data Output  = Dotfiles | Configurations | Simulations | BuildSystems

author :: [Tooling] -> [Output] -> (Determinism, Taste)
author _ _ = (True, "✨fancy✨")
```

If you need something specific, check the repositories.
Everything else is left as an _exercise to the reader_.
