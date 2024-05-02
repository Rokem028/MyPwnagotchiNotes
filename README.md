# MyPwnagotchiNotes

## Intro
This repository will cover some of my notes and my person guide on how to set up a pwnagotcghi with minimal errors


## Hardware

* Raspberry pi zero 2W
* Waveshare E-Ink V4 Display
* Pisugar3
* SD card (over 8GB)

## Flashing
For my chosen image i went for [Jayofelony's image](https://github.com/jayofelony/pwnagotchi/tree/v2.8.9) which has lots of benefits over the standard evilsocket image such as support for the ripi02w, 3, 4, and 5 aswell as having extra standard plugins and a wizard for the config.toml setup

I downloaded the 64 bit version as i have the zero 2W, then simply flash an SD with [Balena Etcher](https://etcher.balena.io/)

### Initial config
After flashing the image you will need to remove and reinsert the card and create a new file in the boot partition of the card, this should be named config.toml and should follow this format which can be found on the [offical pwnagotchi website](pwnagotchi.ai):
```
main.name = "pwnagotchi"
main.lang = "en"
main.whitelist = [
  "EXAMPLE_NETWORK",
  "ANOTHER_EXAMPLE_NETWORK",
  "fo:od:ba:be:fo:od",
  "fo:od:ba"
]

main.plugins.grid.enabled = true
main.plugins.grid.report = true
main.plugins.grid.exclude = [
  "YourHomeNetworkHere"
]

ui.display.enabled = true
ui.display.type = "waveshare_2"
ui.display.color = "black"
```
Then you an eject the card and boot you raspi with the sd, if it doesnt do anything, wait a few minutes as it will be generting its RSA keys on its first boot

## ssh

## ftp

## host connection sharing

## configuring the config

## plugins

