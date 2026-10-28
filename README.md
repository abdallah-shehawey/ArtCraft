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
| [WordCraft](https://github.com/abdallah-shehawey/wordcraft) | [`1027c473`](https://github.com/abdallah-shehawey/wordcraft/commit/1027c473c81b28278436c9aaec934024d2ce5465) | [wordcraft#4369](https://github.com/storytold/wordcraft/pull/4369) Fix window geometry at interface zoom and restore maximized startup (open) |
| [FilmCraft](https://github.com/abdallah-shehawey/filmcraft) | [`631f431b`](https://github.com/abdallah-shehawey/filmcraft/commit/631f431ba8b26b9849f5d95fa7990275f74a83bf) | [filmcraft#3348](https://github.com/storytold/filmcraft/pull/3348) Remember the native window and add GNOME Wayland caption buttons (open) |
| [LightCraft](https://github.com/abdallah-shehawey/lightcraft) | [`0928cd10`](https://github.com/abdallah-shehawey/lightcraft/commit/0928cd104029967cfd8e65db26f1671ee90cce3d) | [lightcraft#3034](https://github.com/storytold/lightcraft/pull/3034) LR-PREF-INTERFACE: Settings › Interface size, Auto or 50–300% (open) |
| [ArtCraft Launcher](https://github.com/abdallah-shehawey/craft-launcher) | [`e14f75c1`](https://github.com/abdallah-shehawey/craft-launcher/commit/e14f75c14b97b0937fd7321301205043c86076f3) | [craft-launcher#904](https://github.com/storytold/craft-launcher/pull/904) Add persistent interface sizing and correct native window restoration (open) |
| [PhotoCraft](https://github.com/abdallah-shehawey/photocraft) | [`453743a0`](https://github.com/abdallah-shehawey/photocraft/commit/453743a0ea7ab1c5b7009aa7278ff3139cafeffd) | [photocraft#9612](https://github.com/storytold/photocraft/pull/9612) Pick up shared window restoration and GNOME Wayland caption buttons (open) |
| [PdfCraft](https://github.com/abdallah-shehawey/pdfcraft) | [`ce921b8d`](https://github.com/abdallah-shehawey/pdfcraft/commit/ce921b8d709137328d44fca514cc295a3caf0368) | [pdfcraft#4760](https://github.com/storytold/pdfcraft/pull/4760) Pick up shared window restoration and GNOME Wayland caption buttons (open) |
| [DeckCraft](https://github.com/abdallah-shehawey/deckcraft) | [`a8223ea4`](https://github.com/abdallah-shehawey/deckcraft/commit/a8223ea42471c5d16cb2154a868f8b65e0dc49e7) | [deckcraft#1407](https://github.com/storytold/deckcraft/pull/1407) Remember the native window and add GNOME Wayland caption buttons (open) |
| [GridCraft](https://github.com/abdallah-shehawey/gridcraft) | [`e9bf271c`](https://github.com/abdallah-shehawey/gridcraft/commit/e9bf271ca3287a1588a906caf82c3d648fe79cba) | [gridcraft#2622](https://github.com/storytold/gridcraft/pull/2622) Remember the native window and add GNOME Wayland caption buttons (open) |
| [SoundCraft](https://github.com/abdallah-shehawey/soundcraft) | [`90361524`](https://github.com/abdallah-shehawey/soundcraft/commit/90361524134529fdc940844278eaa57c999d1ad7) | [soundcraft#1108](https://github.com/storytold/soundcraft/pull/1108) Remember the native window and add GNOME Wayland caption buttons (open) |
| [EffectCraft](https://github.com/abdallah-shehawey/effectcraft) | [`2135f117`](https://github.com/abdallah-shehawey/effectcraft/commit/2135f117684e00a223cac251f7b10b9a1c093773) | [effectcraft#2461](https://github.com/storytold/effectcraft/pull/2461) Remember the native window and add GNOME Wayland caption buttons (open) |
| [DesignCraft](https://github.com/abdallah-shehawey/designcraft) | [`fa407798`](https://github.com/abdallah-shehawey/designcraft/commit/fa407798569a3d9149df28ffa01aed25e5a37869) | [designcraft#1855](https://github.com/storytold/designcraft/pull/1855) Remember the native window and add GNOME Wayland caption buttons (open) |
| [VectorCraft](https://github.com/abdallah-shehawey/vectorcraft) | [`76e5ec86`](https://github.com/abdallah-shehawey/vectorcraft/commit/76e5ec86b9fbfb7cff69d8a532a5d19abb36170a) | [vectorcraft#4228](https://github.com/storytold/vectorcraft/pull/4228) Remember the native window and add GNOME Wayland caption buttons (open) |
| [FigCraft](https://github.com/abdallah-shehawey/figcraft) | [`8033d124`](https://github.com/abdallah-shehawey/figcraft/commit/8033d1244f209b1a196d99cb8f82e43341b0f474) | [figcraft#1364](https://github.com/storytold/figcraft/pull/1364) Remember the native window and add GNOME Wayland caption buttons (open) |
| [CADCraft](https://github.com/abdallah-shehawey/cadcraft) | [`38032016`](https://github.com/abdallah-shehawey/cadcraft/commit/38032016517313b23d9e6339dd10923be2f254ed) | [cadcraft#2194](https://github.com/storytold/cadcraft/pull/2194) Remember the native window and add GNOME Wayland caption buttons (open) |

[storytold/egui#4](https://github.com/storytold/egui/pull/4) is separate: it lets the egui repository's preview job comment on pull requests (`pull-requests: write`).

The shared fork change and its pin still need the owner's approval. FigCraft's second settings store (`app.ron`) is also an owner decision. These contributions remain open PRs. The egui preview job's current permission failure runs the old base workflow; the permission change in #4 takes effect after the owner merges it.

## Review follow-up — 27–28 Oct 2026

[VectorCraft received a human approval](https://github.com/storytold/vectorcraft/pull/4228#pullrequestreview-5664264639) on reviewed head `37470d4`. The integration update below follows that approval and remains available for renewed review. All sixteen pull requests are still open. Final local merge previews on 28 Oct found no conflicts against their live target branches. The shared egui merge and durable dependency pin still require the upstream owner.

Ten contribution branches were updated for upstream changes, retaining window/preferences behavior and regression tests. Eight also reconcile the latest shared `craft-libs` revision while retaining the `egui` restoration pin. SoundCraft retains preference isolation across upstream’s clap startup and captured-environment refactor. LightCraft validates interface-size control patches atomically; EffectCraft validates native window records and rescues X11 positions from disconnected monitors. Validation:

| Project | Validation |
| --- | --- |
| SoundCraft | Workspace fmt and Clippy passed. All workspace test targets executed across CI and continuation (1538 pass results, 1 built-in skip), including captured-environment I/O, control-run geometry and preference-save regressions. One unchanged upstream VST3 fixture fails because it picks the installed 32-bit /usr/lib/libz.so.1 before the loadable 64-bit /lib64 copy. All eight unreached targets, doctests, assets, layers and the 12-crate WASM check passed. Final changes after validation only add Markdown progress/history rows. |
| PhotoCraft | Latest upstream merge passed eight scoped gates: workspace fmt, native desktop and GUI Clippy/tests with HEIF, doctests, layers, scorecard, WASM and translation coverage. Native/GUI tests: 4544 pass results and 20 built-in skips. Full backend/GPU/performance/corpus suites were not rerun; the historical upstream GPU timing failure remains outside this scoped validation. |
| PdfCraft | Full cargo xtask ci exited successfully after the latest upstream OCR/export/dropdown integration: fmt, workspace Clippy, CLI without default features, 5206 test pass results and doctests, translation report, layers, 31-crate WASM, assets and parity passed. The deny stage explicitly skipped its scan because cargo-deny is not installed. Both window-restoration and upstream progress records are retained; the two dependency review threads still require the shared egui merge and durable app pins. |
| WordCraft | Workspace fmt and Clippy passed. All workspace test binaries were executed across full CI and continuation, including the window geometry/maximize regressions. Two unchanged upstream failures remain: IME body epoch assumes a fixed document ID, and multiple-spaced pagination expects a second page on this font environment. Doctests, translation audit, assets, layers and WASM passed in recorded continuation steps. |
| DeckCraft | Full cargo xtask ci passed all eight steps: fmt, PDF dependency policy, workspace Clippy, tests (2116 pass results), doctests, assets, layers and 23-crate WASM check on Linux. |
| VectorCraft | Workspace fmt and Clippy passed; all workspace test binaries executed across full CI and continuation (10502 pass results), including native-record parsing, X11 monitor rescue and control-run geometry isolation. Only the unchanged upstream COLRv1 emoji test failed. Doctests, no-bundled-fonts tests/Clippy and four feature-tree checks, PDF dependencies, assets, brands, cursors, translations, layers and WASM all passed. Final progress/history edits only change Markdown. |
| LightCraft | Fmt, Clippy, HEIF and all workspace tests passed (5230 pass results, 149 built-in data/model/font/GPU/system skips); corrected tracker reference passed parity, layers, assets and WASM in continuation. The new public ui.set atomic-validation regression passed. |
| FilmCraft | Fmt and Clippy passed; startup-memory regression passed. After an artifact-cleanup race and GPU crash in the first gate, all 24 unlaunched integration targets rebuilt and passed, all 41 GPU library tests passed serially, and doctests, layers, assets and WASM passed. |
| DesignCraft | Latest upstream integration passed full cargo xtask ci, all nine steps: fmt, PDF dependencies, workspace Clippy, tests (3484 pass results), translations, doctests, assets, layers and 16-crate WASM check. Both native-window and new upstream progress records are retained. |
| EffectCraft | Full CI completed every stage. New malformed-record and native-X11-position regressions passed. Fmt, workspace Clippy, doctests, PDF dependencies, layers, assets and 32-crate WASM check passed. The same three upstream font/GPU failures remain (two Noto Serif assertions and 15/4159 wide-penumbra pixels); their owning engine/text/GPU sources are unchanged from the merged upstream. Final edits after CI only update Markdown dates/history. |

[DeckCraft's review](https://github.com/storytold/deckcraft/pull/1407#issuecomment-6436351361) ran formatting only. The separate [clipboard PR #1419](https://github.com/storytold/deckcraft/pull/1419) edits the same eframe dependency. A local merge preview found conflicts in both `apps/deckcraft/Cargo.toml` and `Cargo.lock`. Whichever change lands second must keep both `persistence` and `clipboard`, as well as the existing features, then let Cargo update the lockfile while retaining the intended shared egui pin. The combined feature line is:

```toml
eframe = { workspace = true, features = ["persistence", "default_fonts", "wgpu", "accesskit", "clipboard", "links", "wayland", "x11"] }
```

The two PdfCraft dependency threads and the [new VectorCraft dependency review](https://github.com/storytold/vectorcraft/pull/4228#discussion_r4393908478) remain open pending the shared egui merge and owner-approved durable pins. [DesignCraft’s contributor-data review](https://github.com/storytold/designcraft/pull/1855#pullrequestreview-5670942145) requests a generated statistics refresh; its AGENTS.md and docs/contributors.md assign that refresh to maintainers, so this contribution keeps only the contributor’s own opt-in people.toml entry. EffectCraft’s two older native-window review threads are outdated; their fixes and synthetic regressions are published, but the integration could not mark the threads resolved. The egui workflows that require an owner's approval and FigCraft's second settings-store location also remain owner decisions. Linux validation does not establish Windows or macOS behavior.

## Get the code

```sh
git clone --recurse-submodules https://github.com/abdallah-shehawey/ArtCraft.git
```

Cloned without `--recurse-submodules`? Run `git submodule update --init`. The submodules are pinned to the commits above; `.gitmodules` names each contribution branch.

## How it was checked

The contribution branches for all fourteen apps were checked on Fedora 44 (GNOME 50) on 26 Oct. Checks used each app's `cargo xtask ci` or its equivalent steps; PhotoCraft's steps were run individually because cargo-nextest is unavailable. Each PR records the commands, known machine-specific skips and remaining failures. WordCraft and EffectCraft include failures reproduced on their upstream baseline; PhotoCraft retains a laptop GPU timing failure. These are not reported as passing suites. The shared change was also run natively at 150%: repeated normal and maximized reopens, Restore after a maximized restart, and real clicks on the GNOME Wayland caption buttons. macOS and Windows were not run.
