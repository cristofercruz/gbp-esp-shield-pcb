# Game Boy WiFi Printer - D1 Mini Shield  

<a href="https://oshpark.com/shared_projects/KH3ALIwH"><img src="https://oshpark.com/packs/media/images/badge-5f4e3bf4bf68f72ff88bd92e0089e9cf.png" alt="Order from OSH Park"></img></a>

Enthusiasts on the [Game Boy Camera Club discord server](http://bit.ly/gbccd) have been working on a Game Boy Printer emulator project based on ESP8266 D1 mini boards. Taking inspiration from other projects like the [Gameboy Link Cable Breakout PCB](https://github.com/Palmr/gb-link-cable), I created this shield board to add a link connector and pinouts for an oled screen.

The board is designed with two options for the oled screen placement. There are mousebite perferations to trim the board if you plan on using the smaller layout only.

Here's a render of the PCB:  
<img src="images/render.png" alt="3D render of the pcb design" width="50%">

# Recommended D1 mini Boards:  
**LOLIN D1 mini Pro** - https://www.aliexpress.com/item/32724692514.html  
LiPo battery connector, charge circuit included. No power switch.

**LILYGO TTGO D1 mini** - https://www.aliexpress.com/item/4001144115302.html  
16340 battery holder, charge curcuit, and power switch included.

**LOLIN D1 mini** - https://www.aliexpress.com/item/32529101036.html  
No battery connector, charge curcit, or power switch included.

# Components

Besides the OLED and ESP8266 board, there are two components this PCB uses:

* 1x 4.7 KΩ resistor, required
* 1x 3.5 mm LED, optional


Placements for the components are clearly marked on the board's silkscreen. Find the resistor on the bottom of the PCB.

# Configuration

The shield PCB breaks out appropriate pins to the OLED and the printer port. When using the [wifi-gbp-emulator](https://github.com/HerrZatacke/wifi-gbp-emulator) project, include this in your `config.h` file:

```
// GBPrinter shield PCB
// Pinout to OLED
#define USE_OLED
#define OLED_SDA 4
#define OLED_SCL 5
// Pinout to link port
#define SENSE_BOOT_MODE
#define GB_5V_OUT 15
```

You will be able to use the attached OLED, as well as toggle the board to printer mode simply by attaching the link cable to the shield.

When connecting a link cable to the shield, check the silkscreen for indicators on which side should be placed up. (The flat side of the connector should face down and the rounded side should face up, the same side as the OLED screen.)


# Assembled Printer Example:  
Here's a photo of an assembled printer using a D1 mini Pro board:  
<img src="images/assembled.png" alt="Assembled printer using d1 mini pro" width="50%">

You can get help with this project and find info on the software that runs on the ESP by joining the [Game Boy Camera Club discord server](http://bit.ly/gbccd)
