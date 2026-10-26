# ArtCraft contribution workspace

This hub groups my Craft App Suite forks using Git submodules. Each project keeps its own history and upstream pull requests.

**Work in progress:** WordCraft and the shared egui fixes are submitted. The remaining app changes are undergoing local validation before their contribution commits and pull requests are published. Submodules for those apps currently point to their checked-out upstream base commits.

| Fork | Pinned commit | Contribution |
| --- | --- | --- |
| [egui](https://github.com/abdallah-shehawey/egui) | [ba04bd7d](https://github.com/abdallah-shehawey/egui/commit/ba04bd7de66afaba82fd44aa235aa1d060559ee7) | [Upstream PR](https://github.com/storytold/egui/pull/3) |
| [wordcraft](https://github.com/abdallah-shehawey/wordcraft) | [e0d3c29d](https://github.com/abdallah-shehawey/wordcraft/commit/e0d3c29d65bf9675ea22866c8d6298728c64856c) | [Upstream PR](https://github.com/storytold/wordcraft/pull/4369) |
| [filmcraft](https://github.com/abdallah-shehawey/filmcraft) | [7d8dd5ae](https://github.com/abdallah-shehawey/filmcraft/commit/7d8dd5ae782e85c34ddd824a673ffe2adf744c1f) | Local validation in progress |
| [lightcraft](https://github.com/abdallah-shehawey/lightcraft) | [522beb0c](https://github.com/abdallah-shehawey/lightcraft/commit/522beb0c3e6a8521c8298c16209f7db3d84d2608) | Local validation in progress |
| [craft-launcher](https://github.com/abdallah-shehawey/craft-launcher) | [6c5f5ea2](https://github.com/abdallah-shehawey/craft-launcher/commit/6c5f5ea2f5186cefe35797ddacd7d8a866ae2eeb) | Local validation in progress |
| [photocraft](https://github.com/abdallah-shehawey/photocraft) | [5bb85365](https://github.com/abdallah-shehawey/photocraft/commit/5bb853654196eca807212ff8955ba2eb293071ea) | Local validation in progress |
| [pdfcraft](https://github.com/abdallah-shehawey/pdfcraft) | [13bfbd07](https://github.com/abdallah-shehawey/pdfcraft/commit/13bfbd0761e0cbd6abee19093901ea3b012a1e7d) | Local validation in progress |
| [deckcraft](https://github.com/abdallah-shehawey/deckcraft) | [9d23ff97](https://github.com/abdallah-shehawey/deckcraft/commit/9d23ff97b2088ed5b75c9871ceb8d5ebbb91606a) | Local validation in progress |
| [gridcraft](https://github.com/abdallah-shehawey/gridcraft) | [0870b1ad](https://github.com/abdallah-shehawey/gridcraft/commit/0870b1ad1c78f7c83f8983172dda78437a0d9faa) | Local validation in progress |
| [soundcraft](https://github.com/abdallah-shehawey/soundcraft) | [0197e27f](https://github.com/abdallah-shehawey/soundcraft/commit/0197e27fc41ead385783fde4b21090f995e5bb5b) | Local validation in progress |
| [effectcraft](https://github.com/abdallah-shehawey/effectcraft) | [f35634a4](https://github.com/abdallah-shehawey/effectcraft/commit/f35634a4eca5d46f1a10c217c2583942e4703a9e) | Local validation in progress |
| [designcraft](https://github.com/abdallah-shehawey/designcraft) | [18246ddd](https://github.com/abdallah-shehawey/designcraft/commit/18246dddd2c9af3bd062b0e69781a040b34ff9b2) | Local validation in progress |
| [vectorcraft](https://github.com/abdallah-shehawey/vectorcraft) | [3f8d7a0c](https://github.com/abdallah-shehawey/vectorcraft/commit/3f8d7a0c5a54dab4879918375b3955b8d060cdc5) | Local validation in progress |
| [figcraft](https://github.com/abdallah-shehawey/figcraft) | [d2706103](https://github.com/abdallah-shehawey/figcraft/commit/d27061036f9710d86ce39704d1090ebc2c4c8704) | Local validation in progress |
| [cadcraft](https://github.com/abdallah-shehawey/cadcraft) | [004287d9](https://github.com/abdallah-shehawey/cadcraft/commit/004287d91908ae304c665b605c5c6d06df762a3e) | Local validation in progress |

The independent preview-comment permission fix is [storytold/egui#4](https://github.com/storytold/egui/pull/4). Historical runs use the upstream workflow; maintainers must merge that change for future runs.

```sh
git clone --recurse-submodules https://github.com/abdallah-shehawey/ArtCraft.git
```

Each child repository retains its own licences and attribution. Local test profiles, build outputs and private diagnostics are excluded from this hub.
