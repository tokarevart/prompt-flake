# prompt-flake

To use this bash prompt string for your own flake shell add it like so:
```nix
inputs = {
    prompt-flake.url = "github:tokarevart/prompt-flake";
};

devShells.default = pkgs.mkShell {
    shellHook = ''
        ${prompt-flake.devShells.${system}.default.shellHook}
    '';
};
```
