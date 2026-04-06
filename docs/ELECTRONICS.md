# Electronics

Wiring diagram source file: `../hardware/fritzing/kazkar_wiring_diagram.fzz`

## Overview

Казкар is built around an **Arduino Uno**, a **microSD card module**, **three large momentary pushbuttons**, and an **8Ω speaker**. The device was first proven on a breadboard, then integrated into a temporary plastic case, and finally rebuilt into a laser-cut MDF enclosure.

The electronics are prototype-grade. It is not a manufacturing design nor PCB-based. The project is documented honestly as a working prototype: real firmware, real controls, real audio playback, and real enclosure integration.

## Implemented pin mapping

The current sketch uses the following mapping:

### Buttons

- **D5** — Play/Pause
- **D6** — Next
- **D7** — Previous

The buttons are configured as `INPUT_PULLUP`, so each switch is read as active when pressed to ground.

### Audio

- **D9** — speaker output

### microSD module

- **CS** — D4
- **MOSI** — D11
- **MISO** — D12
- **SCK** — D13
- **VCC** — 5V
- **GND** — GND

## Front-panel control layout

The finished enclosure uses this button arrangement:

- **Red** — Play/Pause
- **White** — Previous
- **Green** — Next

The Fritzing wiring diagram reflects the final physical build, including the color-to-function mapping of the front-panel controls. The code itself defines the functions by pin, not by button color.

## Power

Normal portable use was through a **Power Bank 2200** USB battery pack. The attached package and manual list:

- **Capacity:** 2200 mAh
- **Battery type:** lithium-ion
- **Rated input:** DC 5V / 800 mA
- **Rated output:** DC 5V / 800 mA
- **Charging time:** about 3 hours
- **Protection:** built-in protection for short circuit, over-charge, and over-discharge

That power source was used successfully to run the device in normal portable use.

## microSD module notes

The build uses a common 6-pin SPI microSD adapter module with the following labeled pins:

- GND
- VCC
- MISO
- MOSI
- SCK
- CS

The photographed module matches the SPI wiring used by the sketch and the observed prototype build.

## Speaker and audio path

The final build uses an **8Ω speaker** with an approximately **70 mm diameter** and approximately **85 mm screw-hole spacing**.

The Arduino sketch drives audio from **pin 9** using the `TMRpcm` library. The audio files are stored on the microSD card and are expected to be named sequentially, from `song1.wav` through `song11.wav`.

## Firmware note

The sketch comment header has been updated to match the implemented wiring. The code now documents the actual button and SPI pin assignments used by the final build.

## What is not yet included

This repository still does not include:

- PCB layout
- KiCad source
- finalized amplifier stage
- measured runtime testing
- exact original part numbers for every component

The project is fully documented as a working build, while still leaving room for a more formal second-generation hardware revision later.
