# Hi, nerd.

This page intentionally leaves out graphs, badges, and personality quizzes.
If you were looking for flair, it was redirected:
```bash
# contribution graphs, last seen here:
git log --since=1970 | awk '{print $1}' | wc -l > /dev/null
```

I prefer reproducible things. Everything else is best-effort. The write once, cry once part is real, but it tends to outlive your coworkers’ shell scripts, which are still being debugged in production.

```nix
{ ... }@args:
let
  remote = "github.com/inverted-tree";
in {
  imports = [ ../github-profile.nix ];

  environment.repoPackages = with remote; [
    dotfiles
    nixos-config
  ];
  
  system.stateVersion = "25.12";
}
```

```hcl
module "nix_fleet" {
  source = "github.com/inverted-tree/tf-nix-fleet"

  flake = "github:inverted-tree/nixos-config#lab"
  target = "root@${lab_pc.nixos.ipv4_address}"
}
```

Most of what happens between git push and a running machine is automated, repeatable, and intentionally boring. The interesting failures are documented where they belong.

If you need something specific, check the repositories below.
Everything else is left as an _exercise to the reader_.
