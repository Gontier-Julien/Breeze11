# Breeze11 (In progress)

## Overview

Breeze11 is a fork of KDE Breeze decoration with the following changes:

 * The title-bar opacity is configurable.
 * The separator between title-bar and window is removed.
 * Opaqueness, opacity override is added to the exception list properties.
 * Title-bar font is set indpendent from the KDE font settings (for use outside KDE).
 * Rounded Corner like Windows 11.

## Credits

Breeze11 was started from BreezeEnhanced (https://github.com/tsujan/BreezeEnhanced), a former fork of Breeze with title-bar translucency and blurring.

## Dependencies

There are some dependencies you'll need to install. Some people suggested using the following commands:

### Ubuntu, KDE Neon
``` shell
sudo apt install git g++ extra-cmake-modules cmake gettext libkf5config-dev libkdecorations2-dev libqt5x11extras5-dev qtdeclarative5-dev libkf5guiaddons-dev libkf5configwidgets-dev libkf5windowsystem-dev libkf5coreaddons-dev libfftw3-dev
```

### Arch Linux, Manjaro, Antergos
``` shell
sudo pacman -S kdecoration qt5-declarative qt5-x11extras kcoreaddons kguiaddons kconfigwidgets kwindowsystem fftw cmake extra-cmake-modules
```

### OpenSUSE
``` shell
sudo zypper install git extra-cmake-modules libkdecoration2-devel kcoreaddons-devel kguiaddons-devel kconfig-devel kwindowsystem-devel ki18n-devel kconfigwidgets-devel libQt5DBus-devel libqt5-qtx11extras-devel fftw3-devel
```

## Installation

The version number in the file NEWS shows the main version of KWin that is required for the compilation. *Compilation should not be done against other versions of KWin!*.

Open a terminal inside the source directory and do:
```sh
mkdir build && cd build
cmake .. -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Release -DKDE_INSTALL_LIBDIR=lib -DBUILD_TESTING=OFF -DKDE_INSTALL_USE_QT_SYS_PATHS=ON
make
sudo make install
```
After the intallation, restart KWin by logging out and in. Then, Breeze10 will appear in *System Settings &rarr; Application Style &rarr; Window Decorations*.

## Known Issues

None so far.

## Screenshots

![Settings](screenshots/Settings.png?raw=true "Settings")

![Desktop](screenshots/Desktop.png?raw=true "Desktop")
