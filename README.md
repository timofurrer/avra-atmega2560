# avra with ATmega2560 support
> This repository is a clone of avra version 1.3.0 with additional fixes to support the ATmega2560 chip

***

**Original Repository:** http://sourceforge.net/projects/avra/files/1.3.0/
**Avra Version**: 1.3.0
**Platform**: GNU/Linux
*Tested on Debian GNU/Linux*

## Installation

First you have to clone this repository to get the ATmega2560 on linux:

    git clone https://github.com/timofurrer/avra-atmega2560.git avra-atmega2560
    cd avra-atmega2560

After cloning you can configure and compile `avra` with the Makefile in the `src` directory

    cd avra-1.3.0/src/
    ./bootstrap
    ./configure
    make
    make install

*Note: you may need root privileges to install it on your system with `make install`*

## Compile assambler code

You can easily compile your `*.asm` files with the following command:

    avra test.asm

## Flash hex file to controller

To flash the hex file to the controller you need `avrdude`:

    avrdude -p m2560 -c stk600 -U flash:w:test.hex:i
