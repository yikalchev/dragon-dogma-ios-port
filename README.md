# Dragon's Dogma - Dark Arisen — Native on iOS and MacOS

<p align="center"><img src="https://github.com/user-attachments/assets/9a1c9881-2608-499f-944b-c7dcb09acc67" alt="Dragon's Dogma: Dark Arisen — Native on iOS and MacOS" width="100%"></p>

<p align="center"><strong>Unofficial port • No JIT required • Controller supported</strong></p>

Dragon's Dogma: Dark Arisen, the Nintendo Switch edition, running on Apple silicon iPhone, iPad and Mac through a native ARM64 runtime and Metal graphics backend. This is an independent fan project, not an official Capcom or Nintendo release.

## Project status

**First release: v1.0.0.** The initial iOS and macOS builds are prepared for publication. Download them from [Releases](https://github.com/yikalchev/dragon-dogma-ios-port/releases) once the release is published.

### v1.0.0 release notes

- Initial native iOS/iPadOS and macOS builds with independent game-file selection.
- Edge and Classic touch-layout presets, full-screen editor, external controller shortcuts and remapping.
- Full Screen (stretch) and crop modes, adjustable output resolution, MetalFX and selectable anisotropic filtering.
- Portable iOS/macOS save backups with validation and automatic pre-import backup.
- App name: Dragon's Dogma - Dark Arisen. Package names: `DragonsDogma.ipa` and `DragonsDogma-macOS.zip`.

## Features

- Native Apple silicon execution without a runtime JIT.
- Metal graphics, including optional MetalFX spatial upscaling, adjustable output resolution up to 2160p (4K), and 4×/8×/16× anisotropic texture filtering.
- Original aspect ratio, fullscreen crop, or fullscreen stretch.
- Game default, 30 FPS and 60 FPS targets; actual performance depends on device, settings and scene.
- Landscape pre-game launcher with file validation, graphics settings and a deliberate Play button.
- Customizable Edge and Classic touch-controller presets, Nintendo Switch, PlayStation and Xbox button layouts, and button remapping.
- External controller support and visible press/analog feedback while the touch layout is displayed.
- Cross-platform save export and import using `.ddsave` backups (iOS and macOS); old saves are backed up before import.

## Requirements

| Platform | Requirements |
| --- | --- |
| iPhone / iPad | Compatible Apple silicon device, iOS/iPadOS 26 or newer, sufficient free storage, and a compatible method to install the unsigned IPA |
| Mac | Apple silicon Mac, macOS 26 or newer |
| Game | Legally obtained Dragon's Dogma: Dark Arisen Switch base game (NSP/XCI), the matching update and your own console keys |

The prepared build targets the Switch game update **1.0.1 (v65536)**. The launcher checks that the selected game files match the prepared build. Game content and keys are not included in the downloads.

## Installation

### iOS / iPadOS

1. Download `DragonsDogma.ipa` from Releases once available and install it using your preferred compatible sideloading tool.
2. Open the app, then supply the game files and keys in its Documents/game folder using Files, or use **Select game files…** to choose them from another location.
3. For files outside the folder, choose **Copy to game folder** or **Use from current location**. Keep any external storage accessible while playing.
4. Choose your settings, wait for validation to finish, and press **Play**.

### macOS

1. Download `DragonsDogma-macOS.zip` from Releases once available and extract it.
2. Launch **Dragon's Dogma - Dark Arisen.app**.
3. Choose your game folder or individual game files, select a writable storage location, and adjust the pre-game options. Press **Play** to start.

The local Mac package is ad-hoc signed, not notarized. Use only the verified package from this repository's Releases.

## Graphics settings

| Option | Choices |
| --- | --- |
| Frame rate | Game default / 30 FPS / 60 FPS |
| Console mode | Docked / Handheld |
| Output resolution | Match display (recommended) / 720p / 1080p / 1440p / 2160p |
| Screen mode | Original (16:9) / Full Screen (crop) / Full Screen (stretch) |
| Upscaling | Standard / MetalFX (sharper, supported GPUs) |
| Texture filtering | Game default (recommended) / 4× / 8× / 16× |

Output resolution controls the actual presentation drawable, not the game's native internal rendering resolution. Higher output resolution, anisotropic filtering and MetalFX may increase GPU usage, temperature and battery drain.

## Controller shortcuts (iOS)

| Touchscreen | External controller | Action |
| --- | --- | --- |
| Tap controller icon | Double-press L3 | Show / hide touch layout |
| Tap 3D | Double-press R3 | Show / hide analog sticks and L3/R3 |
| Hold controller icon for 3 seconds | Hold L3 for 3 seconds | Open controller menu |
| Hold 3D for 3 seconds | Hold R3 for 3 seconds | Open game settings |

Controller icon colors: **blue** PlayStation, **green** Xbox, **red** Nintendo Switch, **white** neutral/unknown. The icon follows the detected hardware rather than the chosen onscreen layout.

Use the **Customize button size and position** editor to choose Edge or Classic and drag controls. Each preset retains its own positions. Reset restores that preset; Done saves it.

## Saves

Before starting gameplay, use **Saves → Export saves…** to create a portable `.ddsave` file. On the other device, use **Import saves…** and confirm replacement. The app validates the title and backup contents and preserves existing committed saves in a `save-backups` folder before importing. Both platforms use the same archive format; actual in-game migration testing remains ongoing.

## Releases and support

This public repository contains documentation only. The builds will be distributed through [Releases](https://github.com/yikalchev/dragon-dogma-ios-port/releases). Please report reproducible performance or compatibility issues with your device, OS, graphics settings and game scene through [Issues](https://github.com/yikalchev/dragon-dogma-ios-port/issues).

## Credits and legal notices

The runtime builds on the [nxnative](https://github.com/seedds/nxnative) and [Touchline 23](https://github.com/ohxiaoguang/touchline23) projects and their respective upstream components. All original authors retain their rights and attribution. Third-party license requirements apply to any distributed binary; no proprietary game files, console keys, source trees, logs or private development assets are published in this repository.

Dragon's Dogma: Dark Arisen and its trademarks belong to Capcom. This unofficial project is not affiliated with or endorsed by Capcom, Nintendo or Apple.
