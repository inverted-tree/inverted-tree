<h1>
    Hi, nerd.
    <img align="right" src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExazluempoejV4ZzI0MXRnc3p2aWx3dmIyNzk3bTNpZmh0cWtpdzhwMSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/uQ9YH6rSAaS6NlPlnX/giphy.gif" width="50">
</h1>

I work as a **cloud engineer** by day and **homelab architect** by night.
At some point I discovered declarative systems, a strange loop that just wouldn't let me move on.

When working on software projects, I like to motivate my decisions based on the following quote from Antoine de Saint-Exupéry:
> _Perfection is achieved, not when there is nothing more to add, but when there is nothing left to take away._

To some degree, both of these ideas are represented in the technologies I use on a regular basis:

<div align="center">
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/azure/azure-original.svg" alt="Azure" width="48"/>
    &nbsp;&nbsp;&nbsp;
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/terraform/terraform-original.svg" alt="Terraform" width="48"/>
    &nbsp;&nbsp;&nbsp;
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nixos/nixos-original.svg" alt="NixOS" width="48"/>
    &nbsp;&nbsp;&nbsp;
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/podman/podman-original.svg" alt="Podman" width="48"/>
    &nbsp;&nbsp;&nbsp;
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/githubactions/githubactions-original.svg" alt="Actions" width="48"/>
    &nbsp;&nbsp;&nbsp;
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/c/c-original.svg" alt="C" width="48"/>
    &nbsp;&nbsp;&nbsp;
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/lua/lua-original.svg" alt="Lua" width="48"/>
    &nbsp;&nbsp;&nbsp;
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg" alt="Python" width="48"/>
    &nbsp;&nbsp;&nbsp;
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/rust/rust-original.svg" alt="Rust" width="48"/>
</div>
<br>

When it comes to production environments, everything has to be reproducible, or else it's just best-effort.
The write-once cry-once part is real, but it pays off.

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
    system.stateVersion = "26.05";
}
```

If you are here for something specific, chances are it's in one of the repos linked below.
Anything else is left as an _exercise to the reader_.
