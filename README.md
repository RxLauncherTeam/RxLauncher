<meta name="google-site-verification" content="GwYtofooK4Y89IMxFbNN2mJdOfUQI3WYCGlPlQFWvSk" />
<p align="center">
  <img src="assets/standard%20(1).gif" alt="RxLauncher hero banner" style="max-width:100%; height:auto; border-radius:6px;" />
</p>

<h1 align="center">RxLauncher</h1>

<p align="center">
  <img src="assets/20260729_222949.png" alt="RxLauncher logo" width="130" />
</p>

<p align="center">
  <a href="https://discord.gg/9KYDqkuSc3" target="_blank" rel="noopener noreferrer">
    <img src="https://img.shields.io/badge/%F0%9F%92%AC%20Join%20the%20RxLauncher%20Community%20on%20Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="💬 Join the RxLauncher Community on Discord" />
  </a>
</p>

[![Android](https://img.shields.io/badge/Platform-Android-brightgreen.svg?style=flat-square)](https://github.com/RxLauncherTeam/RxLauncher)
[![Java](https://img.shields.io/badge/Java-8%20|%2017%20|%2021-blue.svg?style=flat-square)](https://www.java.com/)
[![License](https://img.shields.io/github/license/RxLauncherTeam/RxLauncher?style=flat-square)](https://github.com/RxLauncherTeam/RxLauncher/blob/main/LICENSE)
[![GitHub release](https://img.shields.io/github/v/release/RxLauncherTeam/RxLauncher?style=flat-square)](https://github.com/RxLauncherTeam/RxLauncher/releases)
[![GitHub stars](https://img.shields.io/github/stars/RxLauncherTeam/RxLauncher?style=flat-square)](https://github.com/RxLauncherTeam/RxLauncher/stargazers)

*Originally inspired by [Boardwalk](https://github.com/zhuowei/Boardwalk).*  RxLauncher is a Minecraft Java Launcher for Android with Fabric, Forge, NeoForge and mod support.

For extended documentation see the project wiki: https://github.com/RxLauncherTeam/RxLauncher/wiki

## Table of Contents

- [Introduction](#introduction)
- [Getting RxLauncher](#getting-rxlauncher)
- [Building](#building)
  - [Quick Build (Recommended)](#quick-build-recommended)
  - [Detailed Build](#detailed-build)
- [Current Status](#current-status)
- [Known Issues](#known-issues)
- [FAQ](#faq)
- [Contributing](#contributing)
- [Support](#support)
- [License](#license)
- [Credits & Dependencies](#credits--dependencies)
- [Roadmap](#roadmap)
- [Project structure](#project-structure)

## Introduction

RxLauncher is an Android launcher that runs Minecraft Java editions on Android devices by bundling mobile OpenJDK builds and necessary native libraries. It supports multiple Minecraft versions and[...]

## Getting RxLauncher

You can obtain RxLauncher in three ways:

1. Releases: Download prebuilt APKs from the stable releases: https://github.com/RxLauncherTeam/RxLauncher/releases
2. CI / automatic builds: See automatic artifacts in Actions: https://github.com/RxLauncherTeam/RxLauncher/actions
3. Build from source (instructions below)

### Quick Build (Recommended)

From a checked-out repository (Linux/macOS):

```bash
# Ensure you have a compatible JDK and Android SDK installed, then:
chmod +x gradlew
./gradlew :app_RXLauncher:assembleDebug
```

On Windows use `gradlew.bat` instead of `gradlew`.

Note: This quick path assumes any required submodules/content (JRE artifacts, native libs) are already present or will be downloaded by Gradle. See the Detailed Build section below for a reproduci[...]

## Building

### Detailed Build

1) Java Runtime Environment (JRE)

- Download the prebuilt JREs for supported architectures from our CI artifacts: https://github.com/RxLauncherTeam/android-openjdk-build-multiarch/actions
- If you need to produce the JRE yourself, follow the instructions in: https://github.com/RxLauncherTeam/android-openjdk-build-multiarch

2) LWJGL / Native components

- The custom LWJGL build and native stubs are documented in: https://github.com/RxLauncherTeam/lwjgl3

3) Generate language list (translations are auto-managed by Crowdin)

- Linux/macOS:

```bash
chmod +x scripts/languagelist_updater.sh
bash scripts/languagelist_updater.sh
```

- Windows:

```batch
scripts\languagelist_updater.bat
```

4) Build GLFW stub (if required):

```bash
./gradlew :jre_lwjgl3glfw:build
```

5) Build the launcher (debug):

```bash
./gradlew :app_RXLauncher:assembleDebug
```

Replace `gradlew` with `gradlew.bat` on Windows.

Notes and tips
- Make sure the Android SDK and required build-tools are installed and available via your environment (ANDROID_HOME/ANDROID_SDK_ROOT).
- If the repository references external modules or submodules (e.g., jre_lwjgl3glfw, app_pojavlauncher), ensure those directories are present or the appropriate submodules are initialized.

## Current Status

- [x] OpenJDK 8 Mobile port: ARM32, ARM64, x86, x86_64
- [x] OpenJDK 17 Mobile port: ARM32, ARM64, x86, x86_64
- [x] OpenJDK 21 Mobile port: ARM32, ARM64, x86, x86_64
- [x] Headless mod installer
- [x] Mod installer with GUI
- [x] OpenGL in OpenJDK environment
- [x] OpenAL (works on most devices)
- [x] Support for Minecraft 1.12.2 and below
- [x] Support for Minecraft 1.13 and above
- [x] Support for Minecraft 1.17 (22w13a) and above
- [x] Game surface zooming
- [x] New input pipe rewritten to native code
- [x] Rewritten controls system

## Known Issues

See the issue tracker for up-to-date issues and their status: https://github.com/RxLauncherTeam/RxLauncher/issues

## FAQ

See the project wiki for frequently asked questions and troubleshooting: https://github.com/RxLauncherTeam/RxLauncher/wiki

## Contributing

We welcome contributions of any kind: code, documentation, translations, bug reports, and feature requests.

- Read our contributing guidelines in the wiki or CONTRIBUTING.md (if present).
- For translations we use Crowdin: https://crowdin.com/project/RXLauncher
- Fork the repository, create a topic branch, and open a pull request describing your changes.
- Use clear commit messages and include testing steps in the PR description.

Code changes should follow the existing style and keep the core functionality unchanged unless the change clearly fixes bugs or improves stability. For large changes, open an issue first to discu[...]

## Support

Join our Discord server for real-time support and community discussions: https://discord.com/invite/aenk3EUvER

## License

RxLauncher is licensed under the GNU Lesser General Public License v3 (LGPLv3). See the LICENSE file for details: https://github.com/RxLauncherTeam/RxLauncher/blob/main/LICENSE

## Credits & Dependencies

- [Boardwalk](https://github.com/zhuowei/Boardwalk) — inspiration and JVM launcher concepts (see their LICENSE and attributions).
- Android Support Libraries — Apache License 2.0
- [gl4es](https://github.com/ptitSeb/gl4es) — MIT License
- [OpenJDK mobile builds](https://github.com/RxLauncherTeam/openjdk-multiarch-jdk8u) — GPLv2+CE (follow the source project license)
- [LWJGL3 (custom)](https://github.com/RxLauncherTeam/lwjgl3) — BSD-3
- [pro-grade](https://github.com/pro-grade/pro-grade) — Apache 2.0
- [bhook](https://github.com/bytedance/bhook) — MIT
- [libepoxy](https://github.com/anholt/libepoxy) — MIT
- [virglrenderer](https://gitlab.freedesktop.org/virgl/virglrenderer) — MIT

Thanks to MCHeads (https://mc-heads.net) for providing Minecraft avatars.

## Roadmap

Current focus:
- Explore new rendering technologies
- Improve stability and performance
- Enhance the mod installation experience

Community feedback is welcome — open issues or start discussions in the repository.

## Project structure

```
/ (root)
  assets/                    images and static assets (app icons, screenshots)
  build.gradle               top-level Gradle file and build configuration
  gradlew, gradlew.bat       Gradle wrapper
  settings.gradle            Gradle settings (note: this project currently sets rootProject.name to 'PojavLauncher' and includes modules named 'app_pojavlauncher' — consider renaming to 'RxLaun[...]
  LICENSE                    project license (LGPLv3)
  README.md                  this documentation
  scripts/                   build helper scripts (language list generator, etc.)
  <modules referenced>      modules such as jre_lwjgl3glfw, app_RXLauncher (may be submodules or directories)
```

How it fits together
- Gradle builds the native JRE artifacts and the Android app modules. Modules referenced in settings.gradle (for example `:jre_lwjgl3glfw`, `:app_pojavlauncher`) are the build targets that produc[...]

## Notes and suggested improvements (no source changes applied by this commit)

- Standardize internal project naming: several files (settings.gradle, module names) still reference "PojavLauncher". Rename modules and update build meta to `RxLauncher` where appropriate to avo[...]
- Verify the wiki link used in earlier README (there were variants like `rxlauncherr.netlify.app` and `RXLauncherteam.github.io`) — this README uses the canonical GitHub wiki and pages; if you [...]
- Consider adding a CONTRIBUTING.md and CODE_OF_CONDUCT.md to the repository to follow open-source best practices.
- Add a simple CI badge for the main workflow (if present) to show build status.
- If the project exposes a reproducible Docker or CI-based environment for building (useful for contributors), document it.

---

If you'd like, I can:
- Create a CONTRIBUTING.md and pull request template.
- Add a CODE_OF_CONDUCT.md and issue/PR templates.
- Open a follow-up PR suggesting renames for `PojavLauncher` references (I will only modify documentation unless you explicitly want code/module rename).
