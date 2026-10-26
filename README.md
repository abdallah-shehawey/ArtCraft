# ArtCraft contributions

One place for my contributions to the [Craft App Suite](https://github.com/storytold). Each folder is a Git submodule pinned to the contribution commit on my fork; each project keeps its own history, licence and upstream pull request.

What the changes do:

- Windows reopen at their last size, or maximized, at any interface size (150% included), and Restore after a maximized restart returns to the last normal size. Before, WordCraft at 150% shrank on every restart.
- On GNOME Wayland, where the compositor draws no frame, windows get standard Adwaita minimize, maximize and close buttons (FilmCraft's were missing).
- LightCraft and the ArtCraft Launcher get a persistent interface size (Auto, or 50–300%); the other apps already had one.

The shared part is [storytold/egui#3](https://github.com/storytold/egui/pull/3); every app PR pins it and depends on it, except LightCraft's: LightCraft already keeps its own window placement, so its PR is the interface size alone.

## Pull requests

| Project | Fork commit | Upstream pull request |
| --- | --- | --- |
| [egui / eframe (shared)](https://github.com/abdallah-shehawey/egui) | [`ba04bd7d`](https://github.com/abdallah-shehawey/egui/commit/ba04bd7de66afaba82fd44aa235aa1d060559ee7) | [egui#3](https://github.com/storytold/egui/pull/3) Fix window restoration across UI zoom and enable GNOME Wayland controls (open)<br>[egui#4](https://github.com/storytold/egui/pull/4) ci: allow the preview job to comment on pull requests (open) |
| [WordCraft](https://github.com/abdallah-shehawey/wordcraft) | [`92db4961`](https://github.com/abdallah-shehawey/wordcraft/commit/92db4961433bd2a299cab136f4744d0778a794bb) | [wordcraft#4369](https://github.com/storytold/wordcraft/pull/4369) Fix window geometry at interface zoom and restore maximized startup (open) |
| [FilmCraft](https://github.com/abdallah-shehawey/filmcraft) | [`7904f71a`](https://github.com/abdallah-shehawey/filmcraft/commit/7904f71a09bd43a5cb4300adf0b35476d0ccd37a) | [filmcraft#3348](https://github.com/storytold/filmcraft/pull/3348) Remember the native window and add GNOME Wayland caption buttons (open) |
| [LightCraft](https://github.com/abdallah-shehawey/lightcraft) | [`e8365d3a`](https://github.com/abdallah-shehawey/lightcraft/commit/e8365d3a56794cd8874ffb3f75ae550a15801fbe) | [lightcraft#3034](https://github.com/storytold/lightcraft/pull/3034) LR-PREF-INTERFACE: Settings › Interface size, Auto or 50–300% (open) |
| [ArtCraft Launcher](https://github.com/abdallah-shehawey/craft-launcher) | [`cd6a3b8b`](https://github.com/abdallah-shehawey/craft-launcher/commit/cd6a3b8bf3378bdd61b07cae136916dc2134efcd) | [craft-launcher#904](https://github.com/storytold/craft-launcher/pull/904) Add persistent interface sizing and correct native window restoration (open) |
| [PhotoCraft](https://github.com/abdallah-shehawey/photocraft) | [`a21d72ec`](https://github.com/abdallah-shehawey/photocraft/commit/a21d72ecc53c2f62b40f2f5abfb1dd7708b93cf5) | [photocraft#9612](https://github.com/storytold/photocraft/pull/9612) Pick up shared window restoration and GNOME Wayland caption buttons (open) |
| [PdfCraft](https://github.com/abdallah-shehawey/pdfcraft) | [`d7abaf46`](https://github.com/abdallah-shehawey/pdfcraft/commit/d7abaf46bb5fd7092b5b7ea5a6845a32002ec635) | [pdfcraft#4760](https://github.com/storytold/pdfcraft/pull/4760) Pick up shared window restoration and GNOME Wayland caption buttons (open) |
| [DeckCraft](https://github.com/abdallah-shehawey/deckcraft) | [`8b96fda5`](https://github.com/abdallah-shehawey/deckcraft/commit/8b96fda56d3372891a778a684ce9261025f2fd0e) | [deckcraft#1407](https://github.com/storytold/deckcraft/pull/1407) Remember the native window and add GNOME Wayland caption buttons (open) |
| [GridCraft](https://github.com/abdallah-shehawey/gridcraft) | [`c2f03e68`](https://github.com/abdallah-shehawey/gridcraft/commit/c2f03e6835cc52bbe91674cc4f35600e845de47e) | [gridcraft#2622](https://github.com/storytold/gridcraft/pull/2622) Remember the native window and add GNOME Wayland caption buttons (open) |
| [SoundCraft](https://github.com/abdallah-shehawey/soundcraft) | [`1c45ace8`](https://github.com/abdallah-shehawey/soundcraft/commit/1c45ace83a4a3bf9d6597ac17a10db19f9d77fd2) | [soundcraft#1108](https://github.com/storytold/soundcraft/pull/1108) Remember the native window and add GNOME Wayland caption buttons (open) |
| [EffectCraft](https://github.com/abdallah-shehawey/effectcraft) | [`6eac2012`](https://github.com/abdallah-shehawey/effectcraft/commit/6eac2012f44d77df01cf82277635d40047a097d4) | [effectcraft#2461](https://github.com/storytold/effectcraft/pull/2461) Remember the native window and add GNOME Wayland caption buttons (open) |
| [DesignCraft](https://github.com/abdallah-shehawey/designcraft) | [`6a0a15c1`](https://github.com/abdallah-shehawey/designcraft/commit/6a0a15c1483eeaba6cb7c017a27d03714a8d50ea) | [designcraft#1855](https://github.com/storytold/designcraft/pull/1855) Remember the native window and add GNOME Wayland caption buttons (open) |
| [VectorCraft](https://github.com/abdallah-shehawey/vectorcraft) | [`78b6f2ea`](https://github.com/abdallah-shehawey/vectorcraft/commit/78b6f2ea22e2c1b60e92e90e95fd857ea02c7778) | [vectorcraft#4228](https://github.com/storytold/vectorcraft/pull/4228) Remember the native window and add GNOME Wayland caption buttons (open) |
| [FigCraft](https://github.com/abdallah-shehawey/figcraft) | [`79fabdf8`](https://github.com/abdallah-shehawey/figcraft/commit/79fabdf8a7b51e389065ef8343151ddddd03594d) | [figcraft#1364](https://github.com/storytold/figcraft/pull/1364) Remember the native window and add GNOME Wayland caption buttons (open) |
| [CADCraft](https://github.com/abdallah-shehawey/cadcraft) | [`fb4fc570`](https://github.com/abdallah-shehawey/cadcraft/commit/fb4fc570866144cd1410b0027cf2773a5779475a) | [cadcraft#2194](https://github.com/storytold/cadcraft/pull/2194) Remember the native window and add GNOME Wayland caption buttons (open) |

[storytold/egui#4](https://github.com/storytold/egui/pull/4) is separate: it lets the egui repository's preview job comment on pull requests (`pull-requests: write`).

## Get the code

```sh
git clone --recurse-submodules https://github.com/abdallah-shehawey/ArtCraft.git
```

Cloned without `--recurse-submodules`? Run `git submodule update --init`. The submodules are pinned to the commits above; `.gitmodules` names each contribution branch.

## How it was checked

Every app ran its own `cargo xtask ci` on Fedora 44 (GNOME 50). The few tests that fail on this machine for reasons outside these changes (installed fonts, the GPU, a system library) are named in each PR. The shared change was also run natively at 150%: repeated normal and maximized reopens, Restore after a maximized restart, and real clicks on the GNOME Wayland caption buttons. macOS and Windows were not run.
