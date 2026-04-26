# The Patch Project

> A free, open-source visual patch library for analog synthesizers — browse, preview, and recreate patches you love.

🌐 **Live App:** [app.edgingtondesmet.com](https://app.edgingtondesmet.com) *(Desktop only — phone support coming soon)*

---

## Table of Contents

- [About](#about)
- [Supported Synths](#supported-synths)
- [Getting Started (Users)](#getting-started-users)
- [Running Locally with GDevelop](#running-locally-with-gdevelop)
- [Contributing](#contributing)
  - [Code of Conduct](#code-of-conduct)
  - [How to Add a New Synth](#how-to-add-a-new-synth)
  - [Submitting a Patch](#submitting-a-patch)
- [Project Structure](#project-structure)
- [License](#license)
- [Disclaimer](#disclaimer)

---

## About

The Patch Project started in early 2025 as **The Crave Patch Project** — born out of frustration. After picking up a Behringer Crave, it was nearly impossible to find patch sheets that were clear, intuitive, and easy to actually use at the synth. So this app was built to fill that gap.

The idea quickly expanded: why stop at one synth? The project was renamed and rebuilt to support a growing collection of instruments, with a focus on making visual patching simple and accessible for everyone — from first-time patcherers to seasoned modular heads.

The app is fully open source under the CC0-1.0 license. Anyone can use it, fork it, or contribute patches and new synth support.

---

## Supported Synths

| Synth | Manufacturer | Status | Patches Available |
|---|---|---|---|
| Crave | Behringer | ✅ Supported | 9 |
| MiniBrute SE | Arturia | 🔧 In Progress | 0 |

> Want to see your synth supported? See [How to Add a New Synth](#how-to-add-a-new-synth) below or [open a Discussion](https://github.com/Connor-ed/The-Patch-Project/discussions).

---

## Getting Started (Users)

No installation required. Head to the live app:

👉 **[app.edgingtondesmet.com](https://app.edgingtondesmet.com)**

From there you can:

1. **Browse** available patches by synth
2. **Preview** a patch sheet to see signal routing at a glance
3. **Recreate** the patch on your physical hardware using the visual guide

> **Note:** The app is currently optimized for desktop and tablet. Mobile/phone support is not yet available.

---

## Running Locally with GDevelop

The Patch Project is built with **[GDevelop](https://gdevelop.io)**, a free, open-source, no-code/low-code game and app engine. You don't need to know traditional programming to work on this project.

### Prerequisites

- [GDevelop](https://gdevelop.io) (free download for Windows, macOS, and Linux)
- [Git](https://git-scm.com/) (to clone the repository)

### Steps

1. **Clone the repository**

   ```bash
   git clone https://github.com/Connor-ed/The-Patch-Project.git
   cd The-Patch-Project
   ```

2. **Open GDevelop** on your machine.

3. **Open the project file** — in GDevelop, click *Open a Project* and navigate to the cloned folder, then into the `Thepatchproject/` subfolder. Select the main GDevelop project file inside it.

4. **Preview the app** — click the *Preview* button in GDevelop's toolbar to launch the app locally in your browser.

5. **Make changes** — edit layouts, assets, or event logic inside GDevelop, then preview again to test.

> All source assets (images, layouts, extensions) are included in the repository so you can get up and running without needing anything external.

---

## Contributing

Contributions of all kinds are welcome — whether that's adding patches for existing synths, fixing bugs, improving layouts, or adding support for a new instrument entirely.

All assets needed to start contributing are included in the [source code](https://github.com/Connor-ed/The-Patch-Project).

### Code of Conduct

Everyone participating in this project is expected to follow the [Contributor Covenant Code of Conduct](https://github.com/Connor-ed/The-Crave-Patch-Project/blob/main/CODE_OF_CONDUCT.md). Please read it before contributing.

---

### How to Add a New Synth

Adding support for a new synthesizer involves a few steps inside GDevelop. Here's the general process:

1. **Fork the repository** and clone your fork locally.

2. **Add a synth layout**
   - In GDevelop, create a new layout (scene) for the synth.
   - Name it clearly (e.g., `Moog_Werkstatt`).
   - Place it in the `layouts/` folder in the project structure.

3. **Create a patch sheet image**
   - Design a clear top-down or front-panel image of the synth that shows all CV/audio jacks, knobs, and patch points.
   - Export it as a `.png` and add it to the `assets/` folder.
   - Numbered patch point images (e.g., `1.png`, `2.png`, ...) are used to indicate individual connections — follow the existing numbering convention used for the Crave.

4. **Build out the patch viewer**
   - Reference the Crave layout as a template for how patch points are mapped to screen coordinates and how patch previews are rendered.
   - Wire up the GDevelop events to show/hide patch connections for each patch in your synth's set.

5. **Add at least one patch** to verify everything works end-to-end.

6. **Open a Pull Request** with a clear description of the synth you've added and any relevant notes.

> Not sure where to start? Drop a message in [Discussions](https://github.com/Connor-ed/The-Patch-Project/discussions) and we're happy to help guide you.

---

### Submitting a Patch

Have a patch you'd like to share with the community? You can submit directly from inside the app — no external form needed.

1. Open the app at [app.edgingtondesmet.com](https://app.edgingtondesmet.com)
2. Press **`Cmd + U`** to open the patch upload dialog
3. Fill in the following fields:
   - **Author name** — your name or handle
   - **Patch name** — a descriptive title (e.g., "Self-oscillating filter drone")
   - **Description** — include any important details about the patch, such as recommended knob positions, what synth it's designed for, or any quirks to be aware of

Submitted patches are reviewed through our moderation pipeline before going live in the app.

---

## Project Structure

```
The-Patch-Project/
└── Thepatchproject/          # Main GDevelop project folder (open this in GDevelop)
    ├── assets/               # Images and visual assets used in the app
    ├── eventsFunctionsExtensions/ # Custom GDevelop extensions/functions
    ├── externalLayouts/      # Shared/reusable layout components
    ├── layouts/              # One layout (scene) per synth + main menu
    └── *.png                 # Numbered patch point images for CV routing visuals
```

---

## License

This project is released under the **[CC0-1.0 License](https://creativecommons.org/publicdomain/zero/1.0/)** — you are free to use, modify, and distribute this project without restriction.

---

## Disclaimer

By using this app at [app.edgingtondesmet.com](https://app.edgingtondesmet.com) or anywhere else on the web, you agree to the [Terms of Service](https://connor.edgingtondesmet.com/the-patch-project-update-log).

All trademarks are the property of their respective owners. **The Patch Project** has no affiliation with Behringer, Arturia, MusicTribe, or any other manufacturer.
