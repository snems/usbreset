# usbreset

Very useful utility if you want to reset some device without physically reconnect it.

Found here:

[https://askubuntu.com/questions/645/how-do-you-reset-a-usb-device-from-the-command-line](https://askubuntu.com/questions/645/how-do-you-reset-a-usb-device-from-the-command-line)

## How to build

__mkdir ./build__

__cd ./build__

__cmake ../__

__make__


## How to use

Select bus and device numbers:

	% lsusb
	Bus 002 Device 002: ID 8087:8002 Intel Corp. 8 channel internal hub
	Bus 002 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
	Bus 001 Device 002: ID 8087:800a Intel Corp. Hub
	Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
	Bus 004 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
	Bus 003 Device 005: ID 0483:3748 STMicroelectronics ST-LINK/V2
	Bus 003 Device 008: ID 0483:5740 STMicroelectronics Virtual COM Port
	Bus 003 Device 004: ID 0c45:7603 Microdia USB Keyboard
	Bus 003 Device 003: ID 30fa:0400 USB OPTICAL MOUSE
	Bus 003 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

And reset it:

	% sudo ./usbreset /dev/bus/usb/003/008
	Resetting USB device /dev/bus/usb/003/008
	Reset successful

