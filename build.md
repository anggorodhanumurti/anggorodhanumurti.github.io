---
layout: page
title: Build
subtitle: How to build Themaphack from source code using Termux
---

_An extensive tutorial is available for building Themaphack using ndk-build within the Termux terminal emulator. Detailed steps are provided:_

### Prepare
We have set up custom [ndk-build](https://github.com/anggorodhanumurti/themaphack/releases/tag/ndk_aide_latest) to work on this project or you can download Android ndk at its [official website](https://developer.android.com/ndk/downloads)
- Download our custom [ndk-build](https://github.com/anggorodhanumurti/themaphack/releases/tag/ndk_aide_latest) tools
- Install [Termux](https://termux.dev/en/) on your Android devices or just use your `terminal/cmd` if you build on PC

~~~
# Update repository Termux
$ pkg update && pkg upgrade -y

# Install required tools
$ pkg install git openssh wget

# Change to Termux $HOME directory
$ cd ~/

# Download ndk-build system
$ wget https://github.com/anggorodhanumurti/themaphack/releases/download/ndk_aide_latest/ndk-build.tar.gz

# Extract ndk-build
$ tar -xvzf ndk-build.tar.gz

# Clone themaphack repository
$ git clone https://github.com/anggorodhanumurti/themaphack.git && cd themaphack

# Run compile script
$ ./compile.sh
~~~ 

> [!NOTE]
> Ensure you select the appropriate library based on your device's architecture. If you're not sure you can check your device architecture using [64bit checker](https://play.google.com/store/apps/details?id=com.danielpolish.a64bitchecker) and download our compiled mod so you dont need to build from source.
- [libs/arm64-v8a](https://github.com/anggorodhanumurti/themaphack/releases/download/v1.1.4-external-64bit/tmhv1.1.4-external-64bit.zip) for 64bit
- [libs/armeabi-v7a](https://github.com/anggorodhanumurti/themaphack/releases/download/v1.1.2-32bit/tmhv1.1.2-32bit.zip) for 32bit

### Installation for External version

_I assume you're using 64bit Android_

1. After `compile.sh` script runs succesfully, lib file will generated on your working directory `libs/arm64-v8a` the filename is `libAkSoundEngine2.so`

2. Open [Zarchiver](https://play.google.com/store/apps/details?id=ru.zdevs.zarchiver) Copy that `libAkSoundEngine2.so` to mlbb folder:
`Android/data/com.mobile.legends/files/dragon2017/assets/comlibs/arm64-v8a`

3. Rename original lib from mlbb **```libAkSoundEngine.bytes```** to **```libTMH.bytes```**

4. Rename **`libAkSoundEngine2.so`** to **`libAkSoundEngine.bytes`** done TMH is installed succesfully! but before open MLBB you must have a key for login to `TMH` modmenu. Generate key [here](https://t0pgamemurah.xyz/freeKey)

> [!WARNING]
> Your account is still not safe from banned. So before you open mlbb game make sure you follow [this guide](https://www.patreon.com/posts/guide-how-to-not-130259867?utm_medium=clipboard_copy&utm_source=copyLink&utm_campaign=postshare_creator&utm_content=join_link)