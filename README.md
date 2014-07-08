# YASEM

Yasem (Yet Another Stb EMulator) is a IPTV Set-Top-Box emulator for desktop platforms.

**YASEM is free software licensed under the term of GPL v2. Some of its components may be licensed under different terms.**

#### How to compile
    
    git clone https://github.com/mvasilchuk/yasem.git
    cd yasem
    git submodule update --init --recursive
    git submodule foreach --recursive git fetch
    git submodule foreach git merge origin master
    qmake
    make

to run

    cd bin
    ./yasem

There is no GUI for application configuring, so, if you need to change settings, go to ~/.config/yasem.

You can use some of command line options:

    --fullscreen - to run App in fullscreen mode
    --developer-tools - to open developer tools on start (the same tools as in Chrome/Chromium)
    
You also may open developer tools anytime from context menu (keep in mind: in current implementation some of portals may override right buttom click, so you may need to open tools before such portal loading).

#### Requirements

* Qt 5 (5.2.1+ is recommended) with Webkit support
* C++11 compatible compiler (tested with GCC and Clang)
* Patched version of [QtAV](https://github.com/wang-bin/QtAV) (included into [yasem-qtav-mediaplayer](https://github.com/mvasilchuk/yasem-qtav-mediaplayer) submodule). See [QtAV requirements](https://github.com/wang-bin/QtAV#requirements).

_WARNING_: Some functionality may not be available with Qt version less than 5.2

- - -

> Copyright &copy; 2013-2014 Maxim Vasilchuk mvasilchuk@gmail.com
