# Hardware Docs

This directory contains any general-purpose documentation related to the way in which this spa hardware works, as well as the hardware we build to interface with the spa pool controller.

## Interfacing with the spa pool

On spa pools containing SV and SV Mini controllers, there exists a port labeled `EXP1` or `EXPAND1` port. This is a standard RJ-45 plug, with the following output coming from the controller on each of the pins:

| Pin | Controller | Wifi Adapter        |
|-----|------------|---------------------|
| 1   | 12V        | 12V                 |
| 2   | GND        | GND                 |
| 3   |            |                     |
| 4   |            |                     |
| 5   | TX         | RX (PIN45 on wifly) |
| 6   | RX         | TX (PIN46 on wifly) |
| 7   | GND        | GND                 |
| 8   | 12V        | 12V                 |

Because the spa is outputting 12V over this connection, we can build our controller with no need for an external power connection - all we need to do is convert the 12V down to a 3.3V voltage suitable for our ESP32 chip.

## Building the hardware

Perhaps in the future we will offer a custom-built solution, but for now you're going to have to get your hands dirty to build out your own piece of hardware. Below we will outline the components you need, as well as how to connect everything together.

> Note: If you lack the confidence to build the hardware yourself, if you want to ask questions, or if you just want to check if anyone near to you already has some components lying around, join the [team discord server](https://discord.gg/faK8Ag4wHn) and introduce yourself!

### Components

| Component | Store links | Comments |
|-----------|-------------|----------|
| ESP32     | [AliExpress](https://www.aliexpress.com/item/1005001929935550.html?spm=a2g0o.order_list.0.0.74be1802hFqod2) | Get 1 already-wielded ESP32 |
| RJ45 connector | [AliExpress](https://www.aliexpress.com/item/1005003717285471.html?spm=a2g0o.order_list.0.0.74be1802hFqod2) | Get a 'H Type+DIP Pins' |
| Buck converter | [AliExpress](https://www.aliexpress.com/item/1005002603013499.html?spm=a2g0o.order_list.0.0.74be1802hFqod2) | Get a '5-40V to 3.3V' converter |
| 330K Resistor | [AliExpress](https://www.aliexpress.com/item/32952657927.html?spm=a2g0o.order_list.0.0.74be1802hFqod2) | You need two 330K ohm resistors |

Beyond these key components, you may want to buy some protoboards, breadboards, pin headers, cables, etc to build your device. Some useful links include:

| Component | Store links | Comments |
|-----------|-------------|----------|
| Pin Headers | [AliExpress](https://www.aliexpress.com/item/32724478308.html?spm=a2g0o.order_list.0.0.74be1802hFqod2) | |