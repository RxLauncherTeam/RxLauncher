<!--
  README for RxLauncherTeam/RxLauncher
  Production-ready, SEO-optimized, non-code changes only.
  Updated image paths and Discord invite per user request.
-->

<p align="center">
  <!-- Animated banner (using assets path provided by maintainer) -->
  <img src="assets/standard%20(1).gif" alt="RXLauncher Animated Banner" style="max-width:100%;height:auto" />
</p>

<h1 align="center">RXLauncher - High Performance Minecraft Java Launcher for Android</h1>

<p align="center">
  <!-- Badges (these use the repo slug RxLauncherTeam/RxLauncher) -->
  <a href="https://github.com/RxLauncherTeam/RxLauncher/releases">
    <img src="https://img.shields.io/github/v/release/RxLauncherTeam/RxLauncher?label=release&style=flat" alt="Release"/>
  </a>
  <a href="https://github.com/RxLauncherTeam/RxLauncher/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/RxLauncherTeam/RxLauncher?style=flat" alt="License"/>
  </a>
  <a href="https://github.com/RxLauncherTeam/RxLauncher/stargazers">
    <img src="https://img.shields.io/github/stars/RxLauncherTeam/RxLauncher?style=flat" alt="GitHub stars"/>
  </a>
  <a href="https://github.com/RxLauncherTeam/RxLauncher/releases">
    <img src="https://img.shields.io/github/downloads/RxLauncherTeam/RxLauncher/total?style=flat" alt="Downloads"/>
  </a>
  <!-- Discord invite (updated) -->
  <a href="https://discord.gg/9KYDqkuSc3" target="_blank" rel="noopener">
    <img src="https://img.shields.io/badge/%F0%9F%92%AC%20Join%20the%20RxLauncher%20Community%20on%20Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Join Discord"/>
  </a>
</p>

<p align="center">
  <!-- Centered project logo (using assets path provided by maintainer) -->
  <img src="assets/20260729_222949.png" alt="RXLauncher Logo" width="160" style="display:block;margin: 12px auto;" />
</p>

---

Table of contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Building from Source](#building-from-source)
- [Supported Versions](#supported-versions)
- [FAQ](#faq)
- [Contributing](#contributing)
- [License](#license)
- [Credits](#credits)
- [Repository Metadata & SEO Recommendations](#repository-metadata--seo-recommendations)

---

## Introduction

RXLauncher is a high-performance, open-source Minecraft Java Edition launcher for Android that supports Fabric, Forge, NeoForge, and modded setups. RXLauncher aims to be a first-class, performant, and user-friendly replacement for mobile Java launchers like PojavLauncher while offering full mod support and an extensible architecture.

Keywords (used naturally in this README): RXLauncher, Minecraft Launcher, Minecraft Java Edition, Android, Fabric, Forge, NeoForge, PojavLauncher Alternative, Open Source, Java Runtime.

RXLauncher is designed for:
- Players who want to run Minecraft Java Edition on Android devices.
- Users who require Fabric and Forge compatibility and robust mod support.
- Developers and contributors looking for an open project built around LWJGL/GLFW or tailored Java runtimes for Android.

---

## Features

- Full support for Minecraft Java Edition on Android devices
- Fabric, Forge and NeoForge mod loader support
- Mod support and easy mod installation paths
- Optimized Java runtime selection for mobile (tailored JRE choices)
- Fast, light-weight, and responsive UX for constrained devices
- Extensible architecture for future mod loaders and runtimes
- Open-source: contributions welcome and traceable
- Focus on stability and compatibility across a wide set of devices

---

## Installation

Note: This repository contains the launcher project and native runtime packaging for LWJGL/GLFW (where applicable). Pre-built releases, APKs, or distribution artifacts (if published) are available on the Releases page.

1. Visit Releases
   - Download the latest APK or build artifact from: https://github.com/RxLauncherTeam/RxLauncher/releases

2. Sideload on Android
   - Enable "Install from unknown sources" on your device (system-dependent).
   - Transfer the APK to your device and install it.
   - Follow the in-app onboarding to download or configure a Java Runtime and Minecraft assets.

3. Mod Support
   - For Fabric/Forge/NeoForge: use the launcher UI to install and manage mod loaders and mods. See the in-app documentation or Releases notes for modloader compatibility.

4. Security
   - Only install APKs from trusted sources (official releases).
   - Verify release checksums/signatures if provided on the Releases page.

---

## Building from Source

This project can be built from source. The following is a generic, high-level build workflow — adapt it to the repository's build system (Gradle/Maven) and any platform-specific steps.

Prerequisites
- Java JDK (version compatible with project)
- Android SDK/NDK (if building an Android APK)
- Android Studio (recommended for APK signing and debugging)
- Gradle (wrapper is typically provided)

Typical steps
1. Clone the repository
   ```bash
   git clone https://github.com/RxLauncherTeam/RxLauncher.git
   cd RxLauncher
   ```

2. Inspect and follow any repository-specific build docs
   - Check `BUILDING.md`, `CONTRIBUTING.md`, or the `docs/` folder (if present) for exact build flags and environment variables.

3. Build using Gradle wrapper (example)
   ```bash
   ./gradlew assembleRelease
   ```
   Or for debug:
   ```bash
   ./gradlew assembleDebug
   ```

4. Install the produced APK on a device
   ```bash
   adb install -r app/build/outputs/apk/release/app-release.apk
   ```

Notes
- Do NOT modify source code or Gradle files if your goal is only packaging or local testing — follow contribution guidelines instead.
- If the project uses native components (LWJGL, JRE pieces), ensure required native libraries are available for target platforms.

---

## Supported Versions

RXLauncher targets the Minecraft Java Edition versions supported by the included mod loaders (Fabric, Forge, NeoForge). Compatibility depends on:
- The Minecraft version selected in the launcher profile.
- The version compatibility of Fabric/Forge/NeoForge and installed mods.

Typical support matrix (check Releases / in-app notes for exact mapping):
- Minecraft Java Edition: common releases (check UI for list)
- Fabric: supported for compatible Minecraft versions (use launcher to choose)
- Forge: supported on matching Minecraft versions
- NeoForge: supported where available

For the latest supported versions, consult the Releases page and project changelog.

---

## FAQ

Q: Is RXLauncher free and open-source?
A: Yes — RXLauncher is open-source. See the LICENSE section below and the LICENSE file in this repository.

Q: Can I install mods?
A: Yes — RXLauncher supports Fabric, Forge, and NeoForge enabling broad mod compatibility. Use the launcher UI to manage mod loaders and mods.

Q: Is this a PojavLauncher alternative?
A: RXLauncher is positioned as a high-performance alternative for running Minecraft Java Edition on Android, with its own approach to runtimes and mod support.

Q: Will RXLauncher get updates for new Minecraft releases?
A: The project aims to keep supporting newer Minecraft Java releases subject to available upstream modloader support (Fabric/Forge/NeoForge).

Q: Where can I get help or report bugs?
A: File an issue in this repository (Issues tab). For live chat, use the Discord community (see the badge above).

---

## Contributing

We welcome contributions! To keep the project stable and discoverable:

1. Fork the repository and create a feature branch.
2. Follow the repository coding and commit conventions.
3. Do not change Gradle or core source files unless implementing a functional improvement. For documentation, packaging, or CI changes, open a PR describing the change.
4. Open a Pull Request with:
   - Summary of the change
   - Why it is needed
   - Testing steps
5. All PRs will be reviewed; maintainers may request changes.

Please read CONTRIBUTING.md (if present) for more details. If there is no CONTRIBUTING.md, follow standard GitHub contribution best-practices.

---

## License

This project is open-source. See the LICENSE file in this repository for full license text.

---

## Credits

- RXLauncherTeam — project maintainers and contributors
- Community contributors and testers
- Third-party projects and libraries used by RXLauncher (Fabric, Forge, NeoForge, LWJGL, etc.)
- Thanks to the broader Minecraft modding and Android launcher communities for guidance and support

---

## Repository Metadata & SEO Recommendations

To maximize GitHub and Google discoverability, apply the following repository settings and files (maintainers or repository admins only):

Recommended GitHub Topics (add to repo settings)
- rxlauncher
- minecraft
- minecraft-java
- minecraft-launcher
- android
- fabric
- forge
- neoforge
- pojavlauncher
- lwjgl
- java
- open-source

About description (max 160 characters)
- RXLauncher - High-performance Minecraft Java Launcher for Android with Fabric, Forge, NeoForge and full mod support.

Website URL (recommend to set if you have one)
- Suggested: https://rxlauncherteam.github.io/RxLauncher (GitHub Pages) or your official product site.
  - If you have a hosted website, set it here (helps SEO).

Social preview image
- Path suggestion: `.github/social-preview.png`
  - Create a 1280x640 PNG that contains the RXLauncher logo + title and set it in the repo settings (Social preview). This improves link previews on GitHub and Google.

Repository keywords (also helpful for SEO & discovery)
- RXLauncher, Minecraft, Minecraft Java Edition, Android Launcher, Fabric, Forge, NeoForge, PojavLauncher Alternative, LWJGL

Other repository presentation suggestions
- Add an explicit `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, and `BUILDING.md` for clearer contributor onboarding and SEO.
- Add release notes and changelog (CHANGELOG.md) for timeline and discoverability by search engines.
- Provide a Social Preview image and high-quality screenshots in `.github/` or `docs/` with descriptive alt text.
- Ensure images referenced in this README are stored in the repo (for example: `.github/banner.gif`, `.github/logo.png`, `.github/social-preview.png`) and referenced by relative paths so GitHub serves them correctly.
- Use descriptive release titles and release notes — include keywords like "RXLauncher", "Minecraft", "Fabric", "Forge" when publishing releases.
- Tag releases with semantic versions and include downloadable APKs and checksums for ease-of-use and trust.

If you would like, I can:
- Produce a ready-to-commit `README.md` file (this content) and a recommended `.github/` image list with suggested filenames.
- Draft short CONTRIBUTING.md and BUILDING.md templates to include in the repo (no source changes).
- Generate suggested issue & PR templates to improve contributor flow and SEO.

Notes & Reminders
- Do NOT modify source code or Gradle files unless you intend to change functionality.
- Verify the Discord invite and replace the placeholder `https://discord.gg/REPLACE_WITH_YOUR_INVITE` with your actual invite URL.
- Place the animated banner and logo in `.github/` (or update paths above) to avoid broken images.

---

Thank you for maintaining RXLauncher — this README optimizes discoverability while preserving your existing project information.
