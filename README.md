# SpaControl

This project provides software and hardware that enables integration and control of spa pools that use the [SV and SV Mini controllers](https://spanet.com.au/spa-controls/), common in spa pools used in Australia and New Zealand. This offers a vastly more cost-effective solution compared with buying a [SV SmartLink WiFi module](https://spanet.com.au/product/sv-smartlink-module-wifi-only/).

Inside this repository you will find the following directories:

* [/hardware](/hardware)
  * [docs](/hardware/docs)
* [/software](/software)
  * [core](/software/core)
  * [esp-basic](/software/esp-basic)
  * [esphome](/software/esphome)
  * [docs](/software/docs)

If you are new to this project, we recommend you read on below to understand what this project is and the requirements, before diving into the docs for both the hardware and software.

## What is this project?

As mentioned, this project aims to provide a hardware and software offering for integrating with the controllers in some spa pools. If you have a spa pool that has an applicable controller, you should read on. If you do not know what kind of controller you use, please file an issue in this repo and we can try to help you find the answer.

Why might you want to introduce this into your spa pool? The primary answer is because it enables for greater home automation abilities for your spa pool. For example, if you run a home automation system, you could write rules to start and stop heating in a far more granular way, perhaps pre-heating in advance of your use, or taking advantage of solar power, and so on. Additionally, it provides you with insight into what your spa pool is doing at any particular time, enabling you to be more informed about its operation and performance. The developers of this project use home automation systems such as [OpenHab](https://www.openhab.org/) and [Home Assistant](https://www.home-assistant.io/), which you may want to look into for your own purposes, before you look at the [/software/docs](/software/docs) directory for additional guidance on integrating into these home automation systems.

You might be wondering why you need to install a hardware device into your spa pool. The answer is that the spa controller does not ship with any integrated wifi module, and this is sold separately. Rather than pay a very large sum of money for this device, some developers have instead chosen to reverse engineer the communication and to build a hardware solution (with embedded software stack) that acts exactly the same as the commercial offering, but at a fraction of the price. This hardware is essentially a programmable WiFi chip, a network jack (for plugging in a standard RJ-45 network cable), and a power converter to power the WiFi chip with power coming over the network cable. There is no need for an external power source - it's simply a network connection inside your spa pool, so it is largely 'plug and play'. Over time there may be more proper hardware offerings available that avoid you needing to solder together the hardware, but for now that is not available. You can learn everything you need to know about the hardware in the [/hardware/docs](/hardware/docs) directory.
