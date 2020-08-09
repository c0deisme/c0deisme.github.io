---
title: Raspberry Pi Zero W Quick Setup
author: c0de
layout: post
category: Raspberry Pi
date: 2020-08-08
---

| Things you will Need | Software you will Need |
| ----------------------- | ------------------------- |
| [Raspberry Pi Zero W](https://amzn.to/3knteau){:target="_blank"} | [Raspberry Pi Imager](https://www.raspberrypi.org/downloads/){:target="_blank"} |
| [Micro SD Card](https://amzn.to/2XJi4Dd){:target="_blank"} | [KiTTY SSH Client](http://www.9bis.net/kitty/){:target="_blank"} or OpenSSH |
| [Mini HDMI to HDMI Adaptor](https://amzn.to/3aak8JG){:target="_blank"} | [Bonjour (Mac and Windows)](https://developer.apple.com/bonjour/){:target="_blank"} |
| [Micro USB to Normal USB Adaptor (Micro USB OTG Adapter)](https://amzn.to/2PCtULa){:target="_blank"} | [Avahi Zeroconf (Linux)](https://wiki.archlinux.org/index.php/Avahi){:target="_blank"} |
| [USB Power Supply](https://amzn.to/2XHtF5X){:target="_blank"} | |
| [USB to Micro USB Cable](https://amzn.to/3fNZn7P){:target="_blank"} | |

## Getting Started

1. Get all the Things you need and Download the Software  
2. Make Sure that your Pi Zero W is Working by connecting the USB cable to the data MicroUSB Port on the Pi and to your PC, if it shows the "BCM2708 Boot" Device it's working.
3. Open Raspberry Pi Imager and Select as OS "Raspberry Pi OS(other)" -> "Raspberry Pi OS Lite (32-bit)" and Choose your SD Card, then click "WRITE"
4. After Writing the SD Card, open the "boot" Volume of the SD Card and add an empty file called "ssh", then edit the config.txt and add this line to the bottom: "dtoverlay=dwc2" and save, now open cmdline.txt and append this after "rootwait": "modules-load=dwc2,g_ether", save that aswell and now eject the SD Card
5. Put the SD Card into your Pi Zero and connect the USB Cable to the data Port again and the other end to your PC, wait 90sec and open your ssh client and connect to "raspberrypi.local" as user "pi" with password "raspberry"
6. Connected to the Pi, enter "sudo raspi-config" and configure youre WiFi settings to connect the Pi Zero to your Network, after thats done reboot the Pi and connect to it using its IP Address
7. PROFIT^^, have fun with your Pi Zero W^^

(all Amazon links are Affiliate Links)  
~c0de
