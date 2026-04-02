# Bill of Materials

This is a practical prototype BOM rather than a manufacturing BOM.

## Core electronics

- 1 × Arduino Uno
- 1 × microSD card adapter / SPI module
- 3 × large momentary pushbuttons with plastic housings/caps
- 1 × 8Ω speaker, approximately 70 mm diameter, with approximately 85 mm screw-hole spacing
- jumper wires / hookup wire
- breadboard or equivalent prototype wiring platform for the early build

## Enclosure / mechanical

- 3.0 mm MDF board
- LightBurn enclosure files
- speaker mounting screws / fasteners

## Power

- 1 × **Power Bank 2200** USB power bank
- **Capacity:** 2200 mAh
- **Battery type:** lithium-ion
- **Rated input:** DC 5V / 800 mA
- **Rated output:** DC 5V / 800 mA
- **Charging time:** about 3 hours
- **Protection:** short circuit / over-charge / over-discharge protection

## Software dependencies

- Arduino IDE
- `SD.h`
- `SPI.h`
- `TMRpcm.h`

## Notes on parts

- The exact original pushbutton part number was not preserved, but the build used standard large momentary pushbuttons with plastic caps/housings.
- The exact original speaker part number was not preserved. Based on the confirmed **8Ω** impedance and approximately **70 mm** diameter, it is documented here as a small full-range hobby speaker in that size class.
- Because the enclosure scale can be adjusted in LightBurn, wire lengths are intentionally not specified as a fixed BOM item.
