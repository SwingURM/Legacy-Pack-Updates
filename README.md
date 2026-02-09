# Legacy Pack Updates

Collection of instructions for improving old modpacks with updated mods.

## About This Patch

This repository provides configuration patches for FTB Infinity Evolved Skyblock.

**Due to lack of explicit permission from FTB Team, this repository does NOT include their configuration files.**

### Changes Included

- Adopted all of glowredman's config modification tips (except EnderIO lang file)
- Added diamond recipe: 1 diamond → 9 Magic Bees diamond nuggets
  - *Reason*: Magic Bees registers its diamond nuggets under the oredict, causing Agricraft to drop its own diamond gem registration and recipe. However, Magic Bees doesn't add a recipe to craft diamond nuggets from diamonds, breaking the original interaction with compressed drawers
- Disabled chisel aeskystone config (crashes on recent test versions)
- Disabled Hodgepodge's eventbus config option (InpureCore)

All other new configurations are auto-generated new config entries. Some configs (like NEI item grouping) were borrowed from the GTNH modpack - thanks to the GTNH community for their contributions.

### How to Apply

1. Download FTB Infinity Evolved Skyblock pack from Curse
2. Extract and navigate to the `overrides` folder
3. Initialize git and commit current state:

   ```bash
   git init
   git add .
   git commit -m "Initial"
   ```

4. Apply the patch:

   ```bash
   git apply /path/to/patch.patch
   ```

## Obtaining Mods

This repository does NOT include mod files. To get mod files, downloader is available at [DreamAssemblerXXL (fork)](https://github.com/SwingURM/DreamAssemblerXXL).

**Note**: Current version requires GitHub and Curse tokens to use. Also, Curse cannot download FTB-Trophy and Decocraft - manual intervention is required.

## Known Issues

- **Silicon Bee disabled**: Magic Bees changed to use presence of silicon dust to determine if silicon bee exists, which disables silicon bee and subsequent Infinity bee etc. No solution yet (may need a patch mod or fork Magic Bees)
- **Infinity Bee dual routes**: After fixing the above issue, there are now two breeding paths leading to the final Infinity bee - reason unknown
- **Ex Nihilo sieve progress async**: The latest release version's 3x3 sieve progress is not synchronized

---

**中文说明**: [README_CN.md](/README_CN.md)

## Index

- [FTB Infinity Evolved Skyblock](/FTB/Infinity_Evolved_Skyblock/README.md)
