armorpaint-pixel
==
![](https://github.com/Vextin/armorpaint-pixel/blob/main/image.png)

This fork adds 32x and 64x texture support to ArmorPaint. It also adds a "pixel art preview" mode under Viewport. 

## Build Instructions
1. Install clang and its dependencies (`sudo apt install clang`)
2. Install gtk 3.0 and its dependencies (`sudo apt install libgtk-3-dev`)
3. From `/armorpaint/paint/` run `../base/make --run`

## Usage Instructions
1. Choose a low resolution during project creation
2. In the toolbar, Viewport->Filter Textures should be OFF
3. For absolute minimal blur, enable Viewport->Pixel Art Preview (forces point filtering, enables texel overlay, uses forward renderer, disables supersampling/SSAO/bloom/vignette/grain/TAA)


![](https://armorpaint.org/img/git_root.jpg)

armorpaint
==============

3D content creation tools.

[armorpaint/](https://github.com/armory3d/armorpaint/tree/main/paint)<br>

**Generating a locale file**
```bash
./base/make --js base/tools/extract_locales.js <locale code>
# Generates a `paint/assets/locale/<locale code>.json` file
```

**Embedding data files**
```bash
# Requires compiler with c23 #embed support (clang 19 or newer)
../base/make --embed
```
