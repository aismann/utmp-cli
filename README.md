# usbtemp-cli
Read temperature from [usbtemp.com](https://usbtemp.com/) USB thermometer.

### How to run it
1. Clone (or download) this repository (and extract files)
2. Run `make` to compile the binary
3. Execute the binary: `./usbtemp-cli`

The output is in degrees Celsius and looks like:
```
May 13 17:05:02 Sensor C: 22.62
```
Date/time formatting is `%b %d %H:%M:%S`.

Instead of compiling from the source, already compiled executable could be downloaded from Releases tab.

### Windows
This application could be also compiled on Windows with a MinGW compiler.

## Usage
```
$ ./usbtemp-cli -h
	-r	Print ROM
	-q	Quiet mode
	-s	Set serial port
```
Serial port could be anything like `/dev/ttyUSB0`, `COM6` or similar.

### Troubleshooting

User, running binary, must have permissions to write to `/dev/ttyUSB0` or similar character device.
Usually, `adduser` to `dialout` group or `chmod o+rw` the character device helps.
