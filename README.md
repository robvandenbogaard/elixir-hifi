# elixir-hifi

Attempt at creating a nice hifi-set appliance using Elixir and Nerves.

## Hardware

* Enclosure is a second hand Aristona cd player with the electronics stripped out
* RaspberryPi 2B
* HifiBerry AMP+
* WIFI adapter
* DVD ROM drive
* USB to SATA adapter
* Speaker connectors (sockets)
* Power adapter for DVD drive, and one for the Pi
* Power strip, connected to the original power button of the cd player
* 40-pin ribbon connector and cable connecting the RPi GPIO to the cd player front (buttons, display, ir sensor)
* IR sensor to GPIO
* OLED Display (64x48)

## Intended functionality

* Display current status, navigation and info
* Hardware buttons can be used to turn power off/on, eject disc, play, pause, stop, next/prev, vol up/down, select mode
* More extensive UI via an IR remote control
* Modes
  * CD Player
  * Internet Radio
  * Streaming from devices (bluetooth/via wifi)
  * Play from library
* Rip CD to library the first time, play from library, use cd to identify what to play

## Architecture

Applications
* Display service
* Button input
* IR input
* Disc
  * Loading
  * ID
  * Audio
  * Rip to library
* Source selector / Playing mode
* Library
* Internet radio
