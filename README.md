# tio - a simple TTY terminal I/O application

[![Build Status](https://travis-ci.org/tio/tio.svg?branch=master)](https://travis-ci.org/tio/tio)
[![Snap Status](https://build.snapcraft.io/badge/tio/tio.snapcraft.svg)](https://build.snapcraft.io/user/tio/tio.snapcraft)

## 1. Introduction

tio is a simple TTY terminal application which features a straightforward
commandline interface to easily connect to TTY devices for basic input/output.

Getting its simplicity, I made two additions:
1) File send capability, to be feasible upgrade a new Database to PS2 ro MSX
   board Converter, that you call ^T K;
2) Test and visualize the full implemention, by using all tools:
  . PS2 to MSX Keyboard Converter;
  . MSX Keyboard Subsystem Emulator and Tester;
  . This functionality shows all MSX Keyboard matrix and shows pressed keys, called by ^T k..
It was created because the author needed a simple no-nonsense TTY terminal
application to easily connect to various terminal TTY devices.

<p align="center">
<img src="https://tio.github.io/images/tio-demo.gif">
</p>


## 2. Usage

The commandline interface is straightforward as reflected in the output from
'tio --help':
```
    Usage: tio [<options>] <tty-device>

    Options:
      -b, --baudrate <bps>        Baud rate (default: 115200)
      -d, --databits 5|6|7|8      Data bits (default: 8)
      -f, --flow hard|soft|none   Flow control (default: none)
      -s, --stopbits 1|2          Stop bits (default: 1)
      -p, --parity odd|even|none  Parity (default: none)
      -o, --output-delay <ms>     Output delay (default: 0)
      -n, --no-autoconnect        Disable automatic connect
      -e, --local-echo            Do local echo
      -l, --log <filename>        Log to file
      -m, --map <flags>           Map special characters
      -v, --version               Display version
      -h, --help                  Display help

    See the man page for list of supported mapping flags.

    In session, press ctrl-t q to quit.
```

The only option which requires a bit of elaboration is perhaps the
`--no-autoconnect` option.

By default tio automatically connects to the provided device if present.  If
the device is not present, it will wait for it to appear and then connect. If
the connection is lost (eg. device is unplugged), it will wait for the device
to reappear and then reconnect. However, if the `--no-autoconnect` option is
provided, tio will exit if the device is not present or an established
connection is lost.

Tio features full bash autocompletion support.

Tio also supports various key commands. Press ctrl-t ? to list the available
key commands.

See the tio man page for more details.


## 3. Installation

The latest release version is available at https://tio.github.io

### 3.1 Installation using release tarball

Install steps:
```
     $ ./configure
     $ make
     $ make install
```
See INSTALL file for more installation details.

### 3.2 Installation using package

Tio comes prepackaged for various GNU/Linux distributions. Visit
https://tio.github.io for package installation details.


## 4. Contributing

Tio is open source. All contributions (bug fixes, doc, ideas, etc.) are
welcome. Visit the tio GitHub page to access latest source code, create pull
requests, add issues etc..

GitHub: https://github.com/tio/tio

Also, if you find this free open source software useful please consider making
a donation:

[![Donate](https://www.paypal.com/en_US/i/btn/x-click-but21.gif)](https://www.paypal.me/lundmar)


## 5. Support

Submit bug reports via GitHub: https://github.com/tio/tio/issues


## 6. Website

Visit https://tio.github.io


## 7. License

Tio is GPLv2+. See COPYING file for license details.


## 8. Authors

Created by Martin Lund \<martin.lund@keep-it-simple.com>

See the AUTHORS file for full list of authors.
