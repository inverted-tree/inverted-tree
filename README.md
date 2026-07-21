<h1>
    Hi, nerd.
    <img align="right" src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExazluempoejV4ZzI0MXRnc3p2aWx3dmIyNzk3bTNpZmh0cWtpdzhwMSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/uQ9YH6rSAaS6NlPlnX/giphy.gif" width="50">
</h1>

Cloud engineer by day, homelab architect by night.
Somewhere in there I fell for declarative systems and never climbed back out.

At work, that's mostly DevSecOps on Azure and Entra.
Managed through IaC and automated pipelines; critical infrastructure doesn't get clicked into existence.
Everything is reproducible, or it's just best-effort.
At home, same instinct, no ticket queue.

<br>
<div align="center">
    &nbsp;&nbsp;&nbsp;
    <a href="https://azure.microsoft.com/" title="Microsoft Azure">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/azure/azure-original.svg" alt="Azure" width="48"/>
    </a>
    &nbsp;&nbsp;&nbsp;
    <a href="https://developer.hashicorp.com/terraform" title="Hashicorp Terraform">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/terraform/terraform-original.svg" alt="Terraform" width="48"/>
    </a>
    &nbsp;&nbsp;&nbsp;
    <a href="https://nixos.org/" title="NixOS">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nixos/nixos-original.svg" alt="NixOS" width="48"/>
    </a>
    &nbsp;&nbsp;&nbsp;
    <a href="https://github.com/features/actions" title="GitHub Actions">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/githubactions/githubactions-original.svg" alt="Actions" width="48"/>
    </a>
    &nbsp;&nbsp;&nbsp;
    &nbsp;&nbsp;&nbsp;
    <a href="https://isocpp.org/" title="C++">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/cplusplus/cplusplus-original.svg" alt="C++" width="48"/>
    </a>
    &nbsp;&nbsp;&nbsp;
    <a href="https://rust-lang.org/" title="Rust">
        <img src="https://www.svgrepo.com/show/374056/rust.svg" alt="Rust" width="48"/>
    </a>
    &nbsp;&nbsp;&nbsp;
    <a href="https://www.lua.org/" title="Lua">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/lua/lua-original.svg" alt="Lua" width="48"/>
    </a>
    &nbsp;&nbsp;&nbsp;
    <a href="https://www.python.org/" title="Python">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg" alt="Python" width="48"/>
    </a>
    &nbsp;&nbsp;&nbsp;
</div>
<br>
<br>

Programming is fun, and personal projects are where I experiment with languages, tools, and ideas that might not survive a production review.

```nix
{ ... }:
let
    remote = "github.com/inverted-tree";
in {
    imports = [ ./github-profile.nix ];

    environment.pinnedRepos = [
        "${remote}/Homelab"
        "${remote}/Dotfiles"
    ];
    system.stateVersion = "26.07";
}
```

Chances are you're after something in the repos below.
Everything else is left as an *exercise to the reader*.