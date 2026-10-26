# ArtCraft contributions

One place for my contributions to the [Craft App Suite](https://github.com/storytold). Each folder is a Git submodule pinned to the contribution commit on my fork; each project keeps its own history, licence and upstream pull request.

What the changes do:

- Windows reopen at their last size, or maximized, at any interface size (150% included), and Restore after a maximized restart returns to the last normal size. Before, WordCraft at 150% shrank on every restart.
- The eframe window store is disabled for runs without preferences and for the affected apps' control-channel runs. SoundCraft and VectorCraft also keep control-run geometry out of their legacy preferences. eframe also finishes writing the window before calling the app's exit hook, including GridCraft's macOS hook that ends the process.
- On GNOME Wayland, where the compositor draws no frame, a native Wayland window with the system frame gets standard Adwaita minimize, maximize and close buttons instead of winit's fallback (FilmCraft's looked broken). Not every app shows them by default: WordCraft, FilmCraft, DeckCraft, SoundCraft, DesignCraft, CADCraft and GridCraft open through XWayland, where GNOME draws the frame, unless `<APP>_WAYLAND=1`; PhotoCraft, PdfCraft, VectorCraft, FigCraft and the launcher draw their own title bar there; and LightCraft's frame is another contributor's PR ([storytold/lightcraft#1928](https://github.com/storytold/lightcraft/pull/1928)).
- LightCraft and the ArtCraft Launcher get a persistent interface size (Auto, or 50–300%); the other apps already had one.

The shared part is [storytold/egui#3](https://github.com/storytold/egui/pull/3); every app PR pins it and depends on it, except LightCraft's: LightCraft already keeps its own window placement, so its PR is the interface size alone.

## Pull requests

| Project | Fork commit | Upstream pull request |
| --- | --- | --- |
| [egui / eframe (shared)](https://github.com/abdallah-shehawey/egui) | [`69750b71`](https://github.com/abdallah-shehawey/egui/commit/69750b71a97dc4672e2fbb70863b838e6795c910) | [egui#3](https://github.com/storytold/egui/pull/3) Fix window restoration across UI zoom and enable GNOME Wayland controls (open)<br>[egui#4](https://github.com/storytold/egui/pull/4) ci: allow the preview job to comment on pull requests (open) |
| [WordCraft](https://github.com/abdallah-shehawey/wordcraft) | [`7fa69be5`](https://github.com/abdallah-shehawey/wordcraft/commit/7fa69be54b5247532c7ab298ef95c99ac0e9c183) | [wordcraft#4369](https://github.com/storytold/wordcraft/pull/4369) Fix window geometry at interface zoom and restore maximized startup (open) |
| [FilmCraft](https://github.com/abdallah-shehawey/filmcraft) | [`1e2db7db`](https://github.com/abdallah-shehawey/filmcraft/commit/1e2db7db417b6f780ceb2f947de2a8bbd1608336) | [filmcraft#3348](https://github.com/storytold/filmcraft/pull/3348) Remember the native window and add GNOME Wayland caption buttons (open) |
| [LightCraft](https://github.com/abdallah-shehawey/lightcraft) | [`ef2c84e8`](https://github.com/abdallah-shehawey/lightcraft/commit/ef2c84e8b99f876add8781d4940c54e587d6bf22) | [lightcraft#3034](https://github.com/storytold/lightcraft/pull/3034) LR-PREF-INTERFACE: Settings › Interface size, Auto or 50–300% (open) |
| [ArtCraft Launcher](https://github.com/abdallah-shehawey/craft-launcher) | [`e14f75c1`](https://github.com/abdallah-shehawey/craft-launcher/commit/e14f75c14b97b0937fd7321301205043c86076f3) | [craft-launcher#904](https://github.com/storytold/craft-launcher/pull/904) Add persistent interface sizing and correct native window restoration (open) |
| [PhotoCraft](https://github.com/abdallah-shehawey/photocraft) | [`8f069bc1`](https://github.com/abdallah-shehawey/photocraft/commit/8f069bc17574323b103f29aa65e110213d51b765) | [photocraft#9612](https://github.com/storytold/photocraft/pull/9612) Pick up shared window restoration and GNOME Wayland caption buttons (open) |
| [PdfCraft](https://github.com/abdallah-shehawey/pdfcraft) | [`38dd2c5c`](https://github.com/abdallah-shehawey/pdfcraft/commit/38dd2c5c7e54c94581d7ee590849e87d685af145) | [pdfcraft#4760](https://github.com/storytold/pdfcraft/pull/4760) Pick up shared window restoration and GNOME Wayland caption buttons (open) |
| [DeckCraft](https://github.com/abdallah-shehawey/deckcraft) | [`55c187b6`](https://github.com/abdallah-shehawey/deckcraft/commit/55c187b66573ede3bce0ad88e822ad6350bc124c) | [deckcraft#1407](https://github.com/storytold/deckcraft/pull/1407) Remember the native window and add GNOME Wayland caption buttons (open) |
| [GridCraft](https://github.com/abdallah-shehawey/gridcraft) | [`e9bf271c`](https://github.com/abdallah-shehawey/gridcraft/commit/e9bf271ca3287a1588a906caf82c3d648fe79cba) | [gridcraft#2622](https://github.com/storytold/gridcraft/pull/2622) Remember the native window and add GNOME Wayland caption buttons (open) |
| [SoundCraft](https://github.com/abdallah-shehawey/soundcraft) | [`d70e4d30`](https://github.com/abdallah-shehawey/soundcraft/commit/d70e4d30398ae664f027e341f353b4de6cc78422) | [soundcraft#1108](https://github.com/storytold/soundcraft/pull/1108) Remember the native window and add GNOME Wayland caption buttons (open) |
| [EffectCraft](https://github.com/abdallah-shehawey/effectcraft) | [`bcfee41d`](https://github.com/abdallah-shehawey/effectcraft/commit/bcfee41dd1d75de7a122dd9d1d5893fcb01c1468) | [effectcraft#2461](https://github.com/storytold/effectcraft/pull/2461) Remember the native window and add GNOME Wayland caption buttons (open) |
| [DesignCraft](https://github.com/abdallah-shehawey/designcraft) | [`454fce51`](https://github.com/abdallah-shehawey/designcraft/commit/454fce51027c88759cb08fd3763d6ee60d441661) | [designcraft#1855](https://github.com/storytold/designcraft/pull/1855) Remember the native window and add GNOME Wayland caption buttons (open) |
| [VectorCraft](https://github.com/abdallah-shehawey/vectorcraft) | [`37470d4e`](https://github.com/abdallah-shehawey/vectorcraft/commit/37470d4ed93fc77bb043f7b505d77cc184841360) | [vectorcraft#4228](https://github.com/storytold/vectorcraft/pull/4228) Remember the native window and add GNOME Wayland caption buttons (open) |
| [FigCraft](https://github.com/abdallah-shehawey/figcraft) | [`8033d124`](https://github.com/abdallah-shehawey/figcraft/commit/8033d1244f209b1a196d99cb8f82e43341b0f474) | [figcraft#1364](https://github.com/storytold/figcraft/pull/1364) Remember the native window and add GNOME Wayland caption buttons (open) |
| [CADCraft](https://github.com/abdallah-shehawey/cadcraft) | [`38032016`](https://github.com/abdallah-shehawey/cadcraft/commit/38032016517313b23d9e6339dd10923be2f254ed) | [cadcraft#2194](https://github.com/storytold/cadcraft/pull/2194) Remember the native window and add GNOME Wayland caption buttons (open) |

[storytold/egui#4](https://github.com/storytold/egui/pull/4) is separate: it lets the egui repository's preview job comment on pull requests (`pull-requests: write`).

The shared fork change and its pin still need the owner's approval. FigCraft's second settings store (`app.ron`) is also an owner decision. These contributions remain open PRs. The egui preview job's current permission failure runs the old base workflow; the permission change in #4 takes effect after the owner merges it.

## Get the code

```sh
git clone --recurse-submodules https://github.com/abdallah-shehawey/ArtCraft.git
```

Cloned without `--recurse-submodules`? Run `git submodule update --init`. The submodules are pinned to the commits above; `.gitmodules` names each contribution branch.

## How it was checked

The contribution branches for all fourteen apps were checked on Fedora 44 (GNOME 50) on 26 Oct. Checks used each app's `cargo xtask ci` or its equivalent steps; PhotoCraft's steps were run individually because cargo-nextest is unavailable. Each PR records the commands, known machine-specific skips and remaining failures. WordCraft and EffectCraft include failures reproduced on their upstream baseline; PhotoCraft retains a laptop GPU timing failure. These are not reported as passing suites. The shared change was also run natively at 150%: repeated normal and maximized reopens, Restore after a maximized restart, and real clicks on the GNOME Wayland caption buttons. macOS and Windows were not run.
