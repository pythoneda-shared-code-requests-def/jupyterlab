# Jupyterlab artifact

Artifact space of <https://github.com/pythoneda-shared-code-requests/jupyterlab>

## How to declare it in your flake

Check the latest tag of the (meta)artifact repository: [https://github.com/pythoneda-shared-code-requests/jupyterlab-artifact-artifact/tags](https://github.com/pythoneda-shared-code-requests/jupyterlab-artifact-artifact/tags) and use it instead of the `[version]` placeholder below.

```nix
{
  description = "[..]";
  inputs = rec {
    [..]
    pythoneda-shared-code-requests-jupyterlab-artifact = {
      [optional follows]
      url =
        "github:pythoneda-shared-code-requests/jupyterlab-artifact-artifact/[version]?dir=jupyterlab-artifact";
    };
  };
  outputs = [..]
};
```

Should you use another PythonEDA modules, you might want to pin those also used by this project. The same applies to [nixpkgs](https://github.com/nixos/nixpkgs "nixpkgs") and [flake-utils](https://github.com/numtide/flake-utils "flake-utils").

Use the specific package depending on your system (one of `flake-utils.lib.defaultSystems`) and Python version:

- `#packages.[system].pythoneda-shared-code-requests-jupyterlab-artifact-python38` 
- `#packages.[system].pythoneda-shared-code-requests-jupyterlab-artifact-python39` 
- `#packages.[system].pythoneda-shared-code-requests-jupyterlab-artifact-python310` 
- `#packages.[system].pythoneda-shared-code-requests-jupyterlab-artifact-python311` 

The Nix flake is under the 
[infrastructure](https://github.com/pythoneda-shared-code-requests/jupyterlab-artifact-artifact/tree/main/jupyterlab-artifact "jupyterlab-artifact") folder in <https://github.com/pythoneda-shared-code-requests/jupyterlab-artifact-artifact>.

