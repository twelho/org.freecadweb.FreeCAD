# org.freecadweb.FreeCAD

This is a fork of the official FreeCAD Flatpak build repository. Its modified to build
the [LinkStable](https://github.com/realthunder/FreeCAD/tree/LinkStable) and [LinkMerge](https://github.com/realthunder/FreeCAD/tree/LinkMerge) branches
of [realthunder's](https://github.com/realthunder) FreeCAD fork.

## Flatpak repository

Pre-built signed nightly Flatpaks from this repo are available at https://twelho.github.io/freecad-realthunder/.

## Build

1. Update submodules: `git submodule update --init --recursive`
2. Install build dependencies: `flatpak install org.kde.Sdk/x86_64/5.15 org.kde.Platform/x86_64/5.15 io.qt.qtwebkit.BaseApp/x86_64/5.15`
3. Build: `flatpak-builder build org.freecadweb.FreeCAD.yaml`

## Create a single-file bundle

- Add to local repo: `flatpak-builder --repo=repo --force-clean --default-branch=ld build org.freecadweb.FreeCAD.yaml`
- Create a single-file bundle: `flatpak build-bundle repo org.freecadweb.FreeCAD.flatpak org.freecadweb.FreeCAD`

## Install

- Install the single-file bundle: `flatpak install org.freecadweb.FreeCAD.flatpak`
