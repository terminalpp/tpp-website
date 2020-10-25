---
title: Installation
layout: titled
---


## `terminalpp`

`terminalpp` supports Windows, Linux and macOS. BSD systems *should* work as well, but are almost never tested. 


**Windows**

Windows 10 version `2004` and above are supported. Older Windows versions from `1909` will most likely work too, but only the latest stable Windows version is regularly tested.

The easiest way is to install `terminalpp` from [Microsoft Store](https://www.microsoft.com/store/apps/9NNH6JQFJ7HD). Additionally, a [MSIX](https://github.com/terminalpp/terminalpp/releases/latest/download/terminalpp.msix) and [MSI](https://github.com/terminalpp/terminalpp/releases/latest/download/terminalpp.msi) installers are provided. The MSIX package is signed by a self-signed [certificate](https://github.com/terminalpp/terminalpp/raw/master/terminalpp.cer).

**Linux**

[Snap](https://snapcraft.io/terminalpp) package is supported on most popular distributions and provides automatic updates. Alternatively, [RPM](https://github.com/terminalpp/terminalpp/releases/latest/download/terminalpp.rpm) and [DEB](https://github.com/terminalpp/terminalpp/releases/latest/download/terminalpp.deb) packages are available. 

Installation from source code is also a viable option, see the [repository](htps://github.com/terminalpp/terminalpp) for details. 

**macOS**

The macOS [app bundle](https://github.com/terminalpp/terminalpp/releases/latest/download/terminalpp-macos.zip) is provided for each version. Only macOS 10.15 and higher are supported.

**Source Code**

For building instructions see the [repository](htps://github.com/terminalpp/terminalpp) for details. On Linux, you can run `sudo make install` after the build to install `terminalpp` properly. 

## `ropen`

`ropen` is only supported on Linux hosts at the moment. [DEB](https://github.com/terminalpp/terminalpp/releases/latest/download/ropen.deb) and [RPM](https://github.com/terminalpp/terminalpp/releases/latest/download/ropen.rpm) packages are provided. To install from source, run the following commands:

    mkdir build-ropen
    cd build-ropen
    cmake .. -DCMAKE_BUILD_TYPE=Release -DINSTALL=ropen -DRENDERER=NONE
    make 
    sudo make install

## `tpp-bypass`

`tpp-bypass` is only supported on WSL distributions and can be installed automatically by `terminalpp` at first execution. 

`tpp-bypass` can be built and installed from source as well:

    mkdir build-tpp-bypass
    cd build-tpp-bypass
    cmake .. -DCMAKE_BUILD_TYPE=Release -DINSTALL=ropen -DRENDERER=NONE
    make 
    mkdir -p $HOME/.local/bin
    cp tpp-bypass/tpp-bypass $HOME/.local/bin









