# Motrix

<a href="https://motrix.app">
  <img src="./static/512x512.png" width="256" alt="App Icon" />
</a>

## A full-featured download manager

[![GitHub release](https://img.shields.io/github/v/release/agalwood/Motrix.svg)](https://github.com/agalwood/Motrix/releases) ![Build/release](https://github.com/agalwood/Motrix/workflows/Build/release/badge.svg) ![Total Downloads](https://img.shields.io/github/downloads/agalwood/Motrix/total.svg) ![Support Platforms](https://camo.githubusercontent.com/a50c47295f350646d08f2e1ccd797ceca3840e52/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f706c6174666f726d2d6d61634f5325323025374325323057696e646f77732532302537432532304c696e75782d6c69676874677265792e737667)

English | [įŽäŊä¸­æ](./README-CN.md)

Motrix is a full-featured download manager that supports downloading HTTP, FTP, BitTorrent, Magnet, etc.

Motrix has a clean and easy to use interface. I hope you will like it đģ.

âī¸ [Official Website](https://motrix.app) | đ [Manual](https://github.com/agalwood/Motrix/wiki)

## đŊ Installation

Download from [GitHub Releases](https://github.com/agalwood/Motrix/releases) and install it.

### Windows

It is recommended to install Motrix using the installation package (Motrix-Setup-x.y.z.exe) to ensure a complete experience, such as associating torrent files, capturing magnet links, etc.

If you use package management tools to manage applications on Windows, such as [Chocolatey](https://chocolatey.org), [scoop](https://github.com/lukesampson/scoop). You can use them to install Motrix.

#### Chocolatey
Thanks to [@Yato](https://github.com/iYato) for continuing to maintain the [Motrix Chocolatey](https://community.chocolatey.org/packages/motrix) package. To install motrix, run the following command from the `command line` or from `PowerShell`:

```bash
# Install
choco install motrix

# Upgrade
choco upgrade motrix
```

#### scoop
If you prefer the portable version, you can use [scoop](https://github.com/lukesampson/scoop) (need Windows 7+) to install Motrix.

```bash
scoop bucket add extras
scoop install motrix
```

### macOS

The macOS users can install Motrix using `brew cask`, thanks to [PR](https://github.com/Homebrew/homebrew-cask/pull/59494) of [@Mitscherlich](https://github.com/Mitscherlich).

```bash
brew update && brew install --cask motrix
```

### Linux

You can download the `AppImage` (for all Linux distributions) or `snap` to install Motrix, see [GitHub/release](https://github.com/agalwood/Motrix/releases) for more Linux installation package formats.

Motrix may need to run with `sudo` for the first time in Linux because there is no permission to create the download session file (`/var/cache/aria2.session`).

If you want to build from source code, please read the **Build** section.

#### AppImage
The latest version of Motrix AppImage requires you to manually perform desktop integration. Please check the documentation of [AppImageLauncher](https://github.com/TheAssassin/AppImageLauncher) .

> Desktop Integration
> Since electron-builder 21 desktop integration is not a part of produced AppImage file.
> [AppImageLauncher](https://github.com/TheAssassin/AppImageLauncher) is the recommended way to integrate AppImages.

Deepin 20 Beta users failed to install Motrix, please follow the steps below:

Open the `Terminal`, paste and run the following command to install Motrix again.

```bash
sudo apt --fix-broken install
```

#### Snap
Motrix has been listed on [Snapcraft](https://snapcraft.io/motrix) , Ubuntu users recommend downloading from the Snap Store.

Tips for v1.5.10

The tray may not display the indicator normally, which makes it inconvenient to exit the application.

Please unchecked Preferences--Basic Settings--Hide App Menu (Windows & Linux Only), click Save & Apply. Then click "Exit" in the File menu to exit the application.

Please update to v1.5.12 and above, you can use the keyboard shortcut <kbd>Ctrl</kbd> + <kbd>q</kbd> to quickly exit the application.

#### AUR
For Arch Linux users, Motrix is available in [aur](https://aur.archlinux.org/packages/motrix/), thanks to the maintainer [@weearc](https://github.com/weearc).

Run the following command to install:

```bash
yay motrix
```

#### Flatpak
Thanks to the [PR](https://github.com/flathub/flathub/pull/2334) of [@proletarius101](https://github.com/proletarius101), Motrix has been listed [Flathub](https://flathub.org/apps/details/net.agalwood.Motrix), Linux users who like the Flatpak can try it.

```bash
# Install
flatpak install flathub net.agalwood.Motrix

# Run
flatpak run net.agalwood.Motrix
```

## â¨ Features

- đš Simple and clear user interface
- đĻ Supports BitTorrent & Magnet
- âī¸ BitTorrent selective download
- đĄ Update tracker list every day automatically
- đ UPnP & NAT-PMP Port Mapping
- đ Up to 10 concurrent download tasks
- đ Supports 64 threads in a single task
- đĨ Supports speed limit
- đļ Mock User-Agent
- đ Download completed Notification
- đģ Ready for Touch Bar (Mac only)
- đ¤ Resident system tray for quick operation
- đ Tray speed meter displays real-time speed (Mac only)
- đ Dark mode
- đ Delete related files when removing tasks (optional)
- đ I18n, [View supported languages](#-internationalization).
- đ  More features in development

## đĨ User Interface

![motrix-screenshot-task-en.png](https://cdn.nlark.com/yuque/0/2020/png/129147/1589782238501-e7b39166-da58-4152-ae34-65a061cafa48.png)

## â¨ī¸ Development

### Clone Code

```bash
git clone git@github.com:agalwood/Motrix.git
```

### Install Dependencies

```bash
cd Motrix
yarn
```

> Error: Electron failed to install correctly, please delete node_modules/electron and try installing again

`Electron` failed to install correctly, please refer to https://github.com/electron/electron/issues/8466#issuecomment-571425574

### Dev Mode

```bash
yarn run dev
```

### Build Release

```bash
yarn run build
```

After building, the application will be found in the project's `release` directory.

## đ  Technology Stack

- [Electron](https://electronjs.org/)
- [Vue](https://vuejs.org/) + [VueX](https://vuex.vuejs.org/) + [Element](https://element.eleme.io)
- [Aria2](https://aria2.github.io/) (Note: macOS and Linux versions use 64-bit aria2c, Windows version uses 32-bit)

## âī¸ TODO

Development Roadmap see: [Trello](https://trello.com/b/qNUzA0bv/motrix)

## đ¤ Contribute [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat)](http://makeapullrequest.com)

If you are interested in participating in joint development, PR and Forks are welcome!

## đ Internationalization

Translations into versions for other languages are welcome đ§! Please read the [translation guide](./CONTRIBUTING.md#-translation-guide) before starting translations.

| Key   | Name                | Status       |
|-------|:--------------------|:-------------|
| ar    | Arabic              | âī¸ [@hadialqattan](https://github.com/hadialqattan), [@AhmedElTabarani](https://github.com/AhmedElTabarani) |
| bg    | ĐŅĐģĐŗĐ°ŅŅĐēĐ¸ŅŅ ĐĩĐˇĐ¸Đē    | âī¸ [@null-none](https://github.com/null-none) |
| ca    | CatalÃ               | âī¸ [@marcizhu](https://github.com/marcizhu) |
| de    | Deutsch             | âī¸ [@Schloemicher](https://github.com/Schloemicher) |
| el    | ÎÎģÎģÎˇÎŊÎšÎēÎŦ            | âī¸ [@Likecinema](https://github.com/Likecinema) |
| en-US | English             | âī¸           |
| es    | EspaÃąol             | âī¸ [@Chofito](https://github.com/Chofito)|
| fa    | ŲØ§ØąØŗÛ               | âī¸ [@Nima-Ra](https://github.com/Nima-Ra) |
| fr    | FranÃ§ais            | âī¸ [@gpatarin](https://github.com/gpatarin) |
| hu    | Hungarian           | âī¸ [@zalnaRs](https://github.com/zalnaRs) |
| id    | Indonesia           | âī¸ [@aarestu](https://github.com/aarestu) |
| it    | Italiano            | âī¸ [@blackcat-917](https://github.com/blackcat-917) |
| ja    | æĨæŦčĒ               | âī¸ [@hbkrkzk](https://github.com/hbkrkzk) |
| ko    | íęĩ­ė´                | âī¸ [@KOZ39](https://github.com/KOZ39) |
| nb    | Norsk BokmÃĨl        |    [@rubjo](https://github.com/rubjo) |
| nl    | Nederlands          | âī¸ [@nickbouwhuis](https://github.com/nickbouwhuis) |
| pl    | Polski              | âī¸ [@KanarekLife](https://github.com/KanarekLife) |
| pt-BR | Portuguese (Brazil) | âī¸ [@andrenoberto](https://github.com/andrenoberto) |
| ro    | RomÃĸnÄ              | âī¸ [@alyn3d](https://github.com/alyn3d) |
| ru    | Đ ŅŅŅĐēĐ¸Đš             | âī¸ [@bladeaweb](https://github.com/bladeaweb) |
| tr    | TÃŧrkÃ§e              | âī¸ [@abdullah](https://github.com/abdullah) |
| uk    | ĐŖĐēŅĐ°ŅĐŊŅŅĐēĐ°          | âī¸ [@bladeaweb](https://github.com/bladeaweb) |
| vi    | Tiáēŋng Viáģt          | âī¸ [@duythanhvn](https://github.com/duythanhvn) |
| zh-CN | įŽäŊä¸­æ             | âī¸           |
| zh-TW | įšéĢä¸­æ             | âī¸ [@Yukaii](https://github.com/Yukaii) |

## đ License

[MIT](https://opensource.org/licenses/MIT) Copyright (c) 2018-present Dr_rOot
