# Ark Species Images

A collection of species images for both Ark: Survival Evolved and Ark: Survival Ascended.
All images consist of a mask and regions so they can be coloured, approximating the look in-game.

## Contributing

Contributions should be via PR. A GitHub Action will automatically check the manifest file within the PR, so please either update the manifest using the below command or allow maintainer edits to the PR so it can be done for you.

To update the manifest to include your images you should install the Python tool [UV](https://docs.astral.sh/uv/getting-started/installation/) and run the following command in the repository directory:
```sh
uvx git+https://github.com/arkutils/obelisk-manager.git update-manifest images/
```

Images contributed to this repository will be made available under MIT license.

## File Naming Scheme

See https://github.com/cadon/ARKStatsExtractor/wiki/Creating-New-Images#file-names for details of the file
naming scheme within ASB.

As a summary, images must be in matching pairs of base colour (`<filename>.png`) and region mask image
(`<filename>_m.png`), where `<filename>` is made up of the following components:
```
<speciesname>[_<ASE|ASA|modid>][_s(m|f)][_p<pattern>][_v<variant>]
```
* `speciesname` is the display name of the species (as showing in ASB and matching the values JSON)
* `ASE|ASA` may be included to only apply to one version of the game.
* `modid` is a numeric ID - either a Steam Workshop ID (for ASE) or a Curseforge Project ID (for ASA)
* `sm` means Male only while `sf` means Female only
* `pattern` is the pattern index, for example for Cat where they have 6 pattern options
* `variant` is the variant index (an integer >0), this can be used to add multiple creature poses the user can chose from

All elements after `speciesname` are optional. The more elements present, the higher priority it will have.
