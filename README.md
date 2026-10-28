![Dragonfly Plate on MPC](https://raw.githubusercontent.com/gmorb/mpc-vst-dragonfly-plate/main/docs/banners/plate.png)

# Dragonfly Plate for MPC OS

An unofficial port of the [Dragonfly Reverb](https://github.com/michaelwillis/dragonfly-reverb) **Plate Reverb** plugin (3.2.10) by Michael Willis and Rob van den Berg, as a native insert effect for Akai MPC and Akai Force standalone devices, **Gen1** (32-bit: Force, MPC Live, Live II, One, X, Key 61) and **Gen2** (64-bit: MPC Live III, One G2, Key G2). A touchscreen page modelled on the original plugin's UI, Q-Link mapping, the original's presets, and full project recall.

A plate reverb with three algorithms (Simple, Nested, Tank), dampening and input filters. 8 presets.

The DSP is upstream's own code, compiled with upstream's own flags, and null-tested against upstream's binary: see [Sound](https://github.com/gmorb/mpc-vst-dragonfly/blob/v1.3.0/docs/SOUND.md).

It shows up in MPC's plugin list as **Plate**, manufacturer **Dragonfly**.

This repo is the plugin's listing in the [MPC OS Plugin Catalog](https://sd88me.github.io/mpc-vst-plugins/). **The source code is in [gmorb/mpc-vst-dragonfly](https://github.com/gmorb/mpc-vst-dragonfly)**, which builds all four Dragonfly reverbs; each release here links to the exact source tag it was built from.

## Install

From the [MPC OS Plugin Catalog](https://sd88me.github.io/mpc-vst-plugins/) (its installers pick the right build for your device), or download from [Releases](../../releases/latest):

| Device | Download |
|---|---|
| Gen1 (32-bit): Force, MPC Live, Live II, One, X, Key 61 | `Plate-<version>-mpc-armv7.zip` |
| Gen2 (64-bit): MPC Live III, One G2, Key G2 | `Plate-<version>-mpc-aarch64.zip` |

Unzip, copy the folder to the device and run `install.sh` as root over SSH (modded firmware or SSH access required); the zip's `INSTALL.md` has the steps, and `uninstall.sh` removes it. The installer refuses the other generation's zip. Both builds have the same parameters and presets, so projects move between generations.

Using the Force VST plugins distribution (`vstscanner.sh`, Gen1)? Use the collection zip from [gmorb/mpc-vst-dragonfly](https://github.com/gmorb/mpc-vst-dragonfly/releases) instead. Use one install method per device: `vstscanner` rebuilds MPC's plugin list and drops plugins added by `install.sh`.

## Controls

| Control | Range | What it does |
|---|---|---|
| Dry Level | 0 to 100% | Level of the unprocessed signal |
| Wet Level | 0 to 100% | Level of the reverb |
| Algorithm | Simple, Nested, Tank | Plate algorithm |
| Width | 50 to 150% | Stereo width of the reverb |
| Predelay | 0 to 100 ms | Time before the reverb starts |
| Decay | 0.1 to 10 s | Decay time of the reverb |
| Low Cut | 0 to 200 Hz | Removes low frequencies from the reverb |
| High Cut | 1000 to 16000 Hz | Removes high frequencies from the reverb |
| Dampen | 1000 to 16000 Hz | Damping (low-pass) of the plate |

## Presets

8 presets: Abrupt Plate, Bright Plate, Clear Plate, Dark Plate, Foil Tray, Metal Roof, Narrow Tank, Phat Tank.

## Q-Links

Q-Link bank: **PLATE** (Dry Level, Wet Level, Width, Predelay, Decay, Low Cut, High Cut, Dampen, Preset, Algorithm).

## Tested

See [`tested.json`](tested.json): the devices and MPC OS versions each release was tested on.

## Source, credits and licence

- Source code, build, tests and changelog: [gmorb/mpc-vst-dragonfly](https://github.com/gmorb/mpc-vst-dragonfly) (each release here names its tag).
- Dragonfly Reverb by Michael Willis and Rob van den Berg; freeverb3 by Teru Kamogashira and others; Noto Sans by Google. Built with [mpc-vst-plugins](https://github.com/sd88me/mpc-vst-plugins).
- GPL-3.0-or-later ([LICENSE](LICENSE)), as Dragonfly Reverb. The release zips include the licence texts and the component notices.
- Not affiliated with or endorsed by the Dragonfly Reverb authors or by Akai Professional / inMusic.

Part of Dragonfly Reverb for MPC OS, with [Hall](https://github.com/gmorb/mpc-vst-dragonfly-hall), [Room](https://github.com/gmorb/mpc-vst-dragonfly-room), [Plate](https://github.com/gmorb/mpc-vst-dragonfly-plate) and [Early Reflections](https://github.com/gmorb/mpc-vst-dragonfly-early-reflections).
