![Dragonfly Plate on MPC](https://raw.githubusercontent.com/gmorb/mpc-vst-dragonfly/main/docs/screenshots/plate.png)

# Dragonfly Plate Reverb for MPC OS

An unofficial port of the [Dragonfly Reverb](https://github.com/michaelwillis/dragonfly-reverb) Plate plugin (3.2.10) by Michael Willis and Rob van den Berg, ported as a native insert effect for **Gen 1 Akai MPC and Akai Force** standalone devices. It features a touchscreen page modelled on the original plugin's UI, Q-Link mapping, 8 presets (plus 3 reverb types), and full project recall.

This plugin recreates the lush, smooth sound of classic plate reverbs—ideal for vocals, drums, and live instrument tracks that need width and warmth without the artificiality of room reflections.

## What Is Plate Reverb?

Plate reverb emulates the sound of a physical metal resonance plate—a sheet of steel or aluminum treated with transducers that vibrate when excited by audio. Unlike algorithmic "hall" or "room" reverbs that simulate acoustic spaces, plate produces a dense, smooth tail with evenly distributed reflections and no distinct early echoes. The result is a rich, shimmering ambiance that sits behind your source without muddying it.

Plate reverb has been a studio staple since the 1950s, featured on countless records from Motown to modern pop. Its signature character is especially suited for:

- **Vocals**: Adds presence and depth without pushing the vocal forward
- **Drums** (especially snare): Creates the classic "big drum" sound with smooth decay
- **Guitars**: Smooths out harsh transients while adding spatial depth
- **Keys and Pads**: Fills out mid-range frequencies with lush ambience

## Controls and Parameters

The Dragonfly Plate interface mirrors the original desktop plugin with a fully functional touchscreen layout and Q-Link assignable parameters:

### Main Pages

- **Decay**: Controls the reverb tail length from short (1.5s) to long (8s). Adjust for tight spaces or vast, washing soundscapes.
- **Pre-Delay**: Sets the time between the direct signal and the onset of reverb (0–200ms). Higher values preserve clarity for transient-heavy sources like snare or vocals.
- **Damping**: Low-pass filters the reverb tail, reducing high-frequency brightness for warmer, older-sounding plates.
- **Diffusion**: Determines how densely reflections are packed. Higher values create smoother, more uniform tails; lower values add texture and character.
- **Mix**: Blends wet/dry signal from 0% (fully dry) to 100% (fully wet).

### Q-Link Assignments

All parameters can be mapped to the MPC's Q-Link knobs for real-time performance control. Default assignments include Decay, Damping, Pre-Delay, and Mix—adjustable per preset via the Q-Link menu.

### Reverb Types

Three distinct plate tonal profiles are available, selectable from the preset menu:

1. **Type A (Classic)**: Bright, smooth, and even—ideal for vocals and orchestral applications
2. **Type B (Warm)**: Darker with reduced high-end shimmer—perfect for guitar and ambient textures
3. **Type C (Open)**: Extended high-frequency response with slightly longer decay—suited for lead instruments and live recordings

### Preset System

Eight user presets are provided, spanning:

- **Vocal plates**: Warm, present, with moderate decay
- **Snare plates**: Short decay, bright tone, strong pre-delay
- **Ambient plates**: Long decay, high diffusion, open tonal character
- **Mix buses**: Subtle plates for glueing drum buses or full mixes

Custom presets can be saved and recalled across sessions. Full project recall preserves all Q-Link mappings and active reverb types.

## Install

Two ways, from the same [Releases](../../releases). Use one per device (see [docs/CATALOG.md](docs/CATALOG.md)).

**From the [MPC OS Plugin Catalog](https://sd88me.github.io/mpc-vst-plugins/)**: download `<Name>-<version>-mpc-armv7.zip` with an `install.sh`; the zip's `INSTALL.md` has the steps.

**Force VST plugins distribution**: download `Dragonfly-Reverb-for-MPC-OS-<version>.zip`. It follows the Force VST plugins distribution layout ([docs/DISTRIBUTION.md](docs/DISTRIBUTION.md)): one self-contained folder per plugin.

Requires a Gen 1 Akai Force or MPC with SSH access (modded firmware such as MockbaMod) and the distribution's `Synths` folder with `vstscanner.sh`. The steps are written for the **Akai Force with MockbaMod**, which mounts its memory card at `/media/662522`:

1. Copy the `Dragonfly - VST - Plate` folder into `/media/662522/Synths` (next to `vstscanner.sh`).
2. On the device: `sh /media/662522/Synths/vstscanner.sh` (afterwards just `vstscanner`). MPC restarts; the plugin is under VST, manufacturer "Dragonfly".

Other custom firmware (for example Hakai), or no `662522` card: put the folder in a `Synths` folder on any drive under `/media` (e.g. `/media/az01-internal/Synths`), find MPC's settings file (`find / -name MPC.settings`), and run `sh <that Synths folder>/vstscanner.sh <settings path>`. The release's README has the full steps, updating from 1.1.x, and troubleshooting.

## Screenshots

| Plate |

![Dragonfly Plate on MPC](https://raw.githubusercontent.com/gmorb/mpc-vst-dragonfly/main/docs/screenshots/plate.png)

## Notes

This is an independent port maintained for the MPC OS community. The original Dragonfly Reverb project is by Michael Willis and Rob van den Berg. No commercial intent—just keeping the dream alive on portable hardware.

---

This is part of the Dragonfly Reverb for MPC OS collection, which also includes Hall, Room, and Early Reflections. This repo focuses specifically on the Plate algorithm.
