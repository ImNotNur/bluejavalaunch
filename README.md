<H1 align="center">BlueJavaLaunch 🔵</H1>

<p align="center">
  <b>Minecraft: Java Edition on Android, finally designed for actual humans (and not just Linux terminal wizards).</b>
</p>

<img src="./app_mojo/src/main/assets/bluejavalaunch.png" align="left" width="150" height="150" alt="BlueJavaLaunch logo">

[![Build APK](https://github.com/ImNotNurgamingYT/BlueJavaLaunch/actions/workflows/build-apk.yml/badge.svg)](https://github.com/ImNotNurgamingYT/BlueJavaLaunch/actions)
[![GitHub commit activity](https://img.shields.io/github/commit-activity/m/ImNotNurgamingYT/BlueJavaLaunch)](https://github.com/ImNotNurgamingYT/BlueJavaLaunch/commits)
[![License: LGPL v3](https://img.shields.io/badge/License-LGPL_v3-blue.svg)](https://www.gnu.org/licenses/lgpl-3.0)

* **BlueJavaLaunch** is a clean, user-friendly fork of [MojoLauncher](https://github.com/MojoLauncher/MojoLauncher) (which is based on [PojavLauncher](https://github.com/PojavLauncherTeam/PojavLauncher)) that lets you play Minecraft: Java Edition on your Android phone or tablet without needing a computer science degree just to configure your settings.
* Tired of mobile launchers looking like a 2004 nuclear reactor control panel—or constantly beefing with each other? Same. So we went full xkcd #927 and made another one. Except this one actually makes sense.
* Runs everything from ancient `rd-132211` builds up to the latest snapshots, with easy support for **Fabric**, **Forge**, **NeoForge**, and **OptiFine**—plus out-of-the-box **Bedrock-style touch controls** so your thumbs don't file a restraining order against you.

## Navigation
- [Why BlueJavaLaunch?](#why-bluejavalaunch)
- [Getting BlueJavaLaunch](#getting-bluejavalaunch)
- [Building](#building)
- [Roadmap](#roadmap)
- [Known Issues](#known-issues)
- [License](#license)
- [Contributing](#contributing)
- [Credits & Third-Party Components](#credits--third-party-components)

## Why BlueJavaLaunch?
* **Zero Jargon by Default:** No more getting jump-scared by `MALLOC_ARENA_MAX` or obscure renderer acronyms on your first boot. BlueJavaLaunch automatically detects your device's RAM and GPU to pick optimal settings silently in the background. *(Don't worry, power users—all the raw JVM flags and renderer toggles are still waiting for you behind the **Nerd Mode** switch).*
* **Bedrock-Styled Touch Controls:** Built-in dynamic floating joystick and clean touch layouts that actually feel natural on a touchscreen.
* **Human Error Messages:** If something crashes, we tell you what actually went wrong in plain English instead of throwing a 500-line Java stack trace at your face and wishing you good luck.
* **Blue > Everything:** Clean, uncluttered, electric-blue UI that respects your screen space.

## Getting BlueJavaLaunch

You can grab BlueJavaLaunch in three ways:

1. **Releases (Recommended):** Download the latest stable APK from the [Releases page](https://github.com/ImNotNurgamingYT/BlueJavaLaunch/releases).
2. **Bleed-Edge Builds:** Grab fresh automated builds straight from [GitHub Actions](https://github.com/ImNotNurgamingYT/BlueJavaLaunch/actions) (click the latest green workflow run and scroll down to **Artifacts**).
3. **Build it Yourself:** Follow the [Building](#building) guide below if you enjoy watching Gradle progress bars.

## Building
Make sure you clone with `--recursive` so the native C/C++ submodules don't go missing:
git clone --recursive [https://github.com/ImNotNurgamingYT/BlueJavaLaunch.git](https://github.com/ImNotNurgamingYT/BlueJavaLaunch.git)
cd BlueJavaLaunch
./gradlew :app_mojo:assembleDebug

If you are building on Windows:
 * Replace ./gradlew with .\gradlew.bat
 * Make sure mojoexec, sdl, and glfw are symlinked into app_mojo/src/main/jni/
(Pro tip: You don't even need Android Studio installed locally—forking this repo and running the included GitHub Actions workflow builds the APK in the cloud for free.)
Roadmap
 * [x] Inherit MojoLauncher's rock-solid core, instance system, and modpack imports
 * [ ] Overhaul Home, Loading, Settings, and Version Switcher into the clean BlueJavaLaunch UI
 * [ ] Smart Auto-RAM and GPU renderer auto-detection on first launch
 * [ ] Native Bedrock-style dynamic floating joystick and smart HUD controls
 * [ ] "Nerd Mode" toggle to hide/unhide raw JVM arguments and renderer overrides
 * [ ] Plain-English crash translator (goodbye, mysterious Exit Code 1)
Known Issues
 * Some physical mice might move at the speed of a sleepy snail.
 * Using Holy GL4ES with massive modpack texture atlases can sometimes stretch textures into modern art.
 * Since this project is brand new, there are probably a few hidden bugs waiting to be discovered—if you find one, open an Issue!
License
 * BlueJavaLaunch is licensed under GNU LGPLv3, staying 100% free and open-source just like its upstream parents.
Contributing
Got an idea to make the UI even cleaner, spotted a typo, or want to help translate the launcher into more languages? Pull requests and issues are always welcome! Keep the code clean, keep the UI human, and explain what your PR changes.
Credits & Third-Party Components
Huge shoutout to the MojoLauncher and PojavLauncher teams for doing all the heavy lifting that makes Java Edition on Android possible in the first place:
 * MojoLauncher: GNU LGPLv3 License
 * PojavLauncher: GNU LGPLv3 License
 * Android Support Libraries: Apache License 2.0
 * Holy GL4ES: MIT License
 * OpenJDK: GNU GPLv2 License
 * GLFW: zlib license
 * SDL: zlib license
 * LWJGL2-GLFW: 3-Clause BSD license
 * LWJGL3: BSD-3 License
 * mojoexec: MIT License
 * Mesa 3D Graphics Library: MIT License
 * pro-grade: Apache License 2.0
 * Authlib-Injector: AGPL-3.0
 * alsoft: GNU LGPL and Modified PFFFT
 * oboe: Apache License 2.0
 * Thanks to Mineskin for providing Minecraft avatars.
 * This is vibecoded lol but temporarily

