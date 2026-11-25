# baras-flake for Nix Users


Add the following to your `flake.nix`:
```nix
inputs = {
  baras = {
    url = "github:baras-app/baras";
  };
  # ...
}
```

Then add the following in `environment.systemPackages` from your `configuration.nix` : 
```nix
inputs.baras.packages.${pkgs.stdenv.hostPlatform.system}.
```

Tested and working on NixOs (x86_64-linux) with Niri & Noctalia.
Feel free to open an issue if you encounter any issue !
