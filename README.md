# nixos for macos

install nixos with the normal installation instructions eg [the curl command](https://nixos.org/download/)

enable flakes
```
    mkdir -p ~/.config/nix
    cd ~/.config/nix
    touch nix.conf
    # add `experimental-features = nix-command flakes` to nix.conf
```

copy flake to ~/.config/nix-darwin

[install nix-darwin ](https://github.com/LnL7/nix-darwin?tab=readme-ov-file#flakes)


## Issues

### nix channels Using mismatched versions Home Manager version 24.05 and Nixpkgs version 24.11
nix-channel --remove nixpkgs
nix-channel --add https://nixos.org/channels/nixpkgs-24.05-darwin nixpkgs
nix-channel --update
home-manager switch