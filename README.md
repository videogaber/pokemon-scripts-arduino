# Pokemon Scripts for Arduino

## Introduction
Since the Nintendo Switch now supports USB controllers, some enterprising individuals reverse-engineered the Pokken Tournament Pro Pad firmware for use on microcontrollers. This repository is a collection of scripts which execute input loops on the controller that allow for automating repetitive tasks in Pokemon Sword & Shield, such as hosting raids and hatching eggs.

## Instructions
* You will need to have `avr-gcc` installed on your system
* In the `makefile`, change the `TARGET` to the script you'd like to build
* Ensure that the `MCU` is set the the appropriate chipset for your microcontroller (for example, `atmega16u2` for an Arduino UNO R3)
* Run `make`
* Flash the resulting `.hex` file to your microcontroller

The instructions for putting your microcontroller in DFU mode and flashing firmware differ depending on your hardware, so those instructions will not be included here.

## Scripts
* **DaySkipper_US**: Auto day-skipper for US date arrangement (mm/dd/yyyy hh:mm:AM)
* **DaySkipper_EU**: Auto day-skipper for EU date arrangement (dd/mm/yyyy hh:mm)
* **DaySkipper_JP**: Auto day-skipper for JP date arrangement (yyyy/mm/dd hh:mm)
* **DaySkipper_US_NoLimit**: DaySkipper_US but without 22280 days limit
* **DaySkipper_EU_NoLimit**: DaySkipper_EU but without 22280 days limit
* **DaySkipper_JP_NoLimit**: DaySkipper_JP but without 22280 days limit
* **AutoNthDaySkipper**: Auto roll den to the nth day, SR and repeats
* **AutoLoto**: Infinite loto reward grinding
* **AutoFossil**: Shiny Fossil grinding
* **AutoHost**: Auto hosting raids, with optional fixed/random link code, using game restart to exit
* **AutoHostWithFriendAccept**: Auto hosting raids, using game restart to exit, and adding friends betweenraids
* **AutoHostAirplane**: Auto hosting raids, using airplane mode method to exit
* **AutoHostAirplaneWithFriendAccept**: Auto hosting raids, using airplane mode method to exit, and adding friends between raids
* **TurboA**: A button masher (for digging duo)
* **WattFarmer**: Fast watt collector
* **BerryFarmer**: Fast berry farmer
* **BoxRelease**: Release all pokemon in PC boxes
* **Hatcher**: Automatically collect and hatch eggs
* **RemoveFriends**: Quickly remove as many friends as you'd like

Each of these have instructions written in a comment at the top of the corresponding `.c` file.

## Pre-Compiled Hexes
In the build folder, you will find precompiled hexes for the scripts that don't require variables to be changed.  These include:
* AutoNthDaySkipper (set to 3 days)
* AutoLoto
* AutoHost (No Link Code)
* AutoHostWithFriendAccept (No Link Code)
* AutoHostAirplane (No Link Code)
* AutoHostAirplaneWithFriendAccept (No Link Code)
* TurboA
* WattFarmer
* BerryFarmer
* BoxRelease

Additionally, there are precompiled hexes for hatching eggs of Pokemon that require 5120 steps or 6400 steps. Note that these both assume you have the Oval Charm and a Pokemon with Flame Body in your party in a slot other than the 2nd.

**Note that these builds are for `atmega16u2` boards such as the Arduino UNO R3. They will not work if your board has a different chipset!**

## Contributing
Feel free to submit a pull-request with a clear explanation of what improvement you are adding. I will review it as quickly as I can.

## Credits
These scripts originate from various people, and have been tweaked, modified and optimized along the way. As more contribute, I'll try and keep this list up-to-date.

* [progmem](https://github.com/progmem)
* [shinyquagsire](https://github.com/shinyquagsire23)
* [bertrandom](https://github.com/bertrandom)
* [hoskinsw](https://github.com/hoskinsw)
* [brianuuuSonic](https://www.youtube.com/channel/UCHV0EP9TifKSo7RERIbY1QA)
* [plus](https://www.youtube.com/channel/UCHV0EP9TifKSo7RERIbY1QA)
* [Pedro](https://www.youtube.com/channel/UCHV0EP9TifKSo7RERIbY1QA)
