# Hi, nerd.

This page intentionally leaves out graphs, badges, and personality quizzes.
If you were looking for flair, it was redirected:
```bash
# contribution graphs, last seen here:
git log --since=1970 | awk '{print $1}' | wc -l > /dev/null
# sorry, I piped them to /dev/null to save disk space.
```

I prefer reproducible things. The rest is incidental.
```bash
set -euo pipefail

alias editor="vim"
alias system="nix"
alias build="ninja"

# policy:
#   - if it isn't reproducible, it isn't done
#   - if it needs a badge, it probably doesn't
#   - if it works, commit before asking why
```

Minimal description, maximum signal.
```haskell
-- not a library, just an interface promise
module Profile where

type Determinism = Bool
type Taste = "plain"

data Tooling = Vim | NixOS | Ninja deriving (Eq, Show)
data Output  = Dotfiles | Configurations | Simulations | BuildSystems

author :: [Tooling] -> [Output] -> (Determinism, Taste)
author _ _ = (True, "plain")
```

A few notes for the curious:
```bash
# dotfiles:
#   predictable inputs → predictable edits
# nix:
#   state described, not inferred
# ninja:
#   do the minimum necessary; do it fast
# c:
#   the language God intended
# rust:
#   for days when you can’t check every printf()
#   and someone starts shouting about memory safety
# simulations:
#   floating point will have opinions; that’s fine
```

FAQ (rarely asked, still answered):
```text
Q: Where are the top languages?
A: Hidden behind an interface. Implementation detail.

Q: Why no contribution heatmap?
A: Rate limiting applied at /dev/null.

Q: Is there a theme?
A: Determinism over decoration.
```

If you need something specific, check the repositories.
Everything else is left as an exercise to the reader.
