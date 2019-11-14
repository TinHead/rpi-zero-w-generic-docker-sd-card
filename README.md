[![Build Status](https://cloud.drone.io/api/badges/TinHead/rpi-zero-w-generic-docker-sd-card/status.svg)](https://cloud.drone.io/TinHead/rpi-zero-w-generic-docker-sd-card)


# What is this?
This repo is used to build a generic raspberry pi zero w SD Card image which is setup 

This repo makes use of the docker image build from https://github.com/TinHead/rpi-sd-builder on https://drone.io to generate a Raspberry Pi Zero W sd card image whch cotains:

- rpi0w firmware and kernel from raspberry github
- systemd as init system
- docker
- wpa-supplicant and tools to get wifi going 
- customisations from the overlay here

Wifi is setup as Access Point by default:

- network ssid: bot
- network pass: bot123456
_
There is a script which runs on boot and checks for /boot/wifi_network_conf file which should look like:

```text
network: mynetwork
pass: mynetworkpass
```

If the file is found the network is added to wpa-supplicant and AP is disabled.

# How to use?

The default build id going to create a github release with the sd card image if the build is successful.
You can downaload the images from the Releases section of this repo.

If you want to customize the build ... I'll add info on that later... 


