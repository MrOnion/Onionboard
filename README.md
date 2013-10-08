
# Onionboard PCB for FreeEMS

This PCB is intended to be used in conjunction with a separate microcontroller module to create a basic engine management system. It has a simple power supply and enough general purpose I/O to get started. Basically any microcontroller and software combo can be used but it is particulary designed to be used with the open-source FreeEMS project.

http://freeems.org/

Its ideal for people who wants to experiment and learn about the world of engine management.

The project is done with CadSoft Eagle version 6.x and is within the freeware limitations.

http://www.cadsoftusa.com/download-eagle/freeware/

## Features

* 2-Layer PCB
* Size is about 10x10cm (fits in a euro case)
* 5V LDO regulated power supply with VDR protection
* 2 Polyfuse protected 5V reference voltage outputs
* 4 auto-protected injector outputs (high impedance only)
* 2 auto-protected accessory outputs
* 4 mosfet drivers for ignition amplifiers (5V or 12V)
* 4 protected A/D inputs
* 4 protected temperature inputs (can be used as normal A/D)
* 2 protected on/off switch inputs
* 2 ground loop monitor inputs
* CEL LED and run/load switch for FreeEMS

One thing to point out is that at this stage the board DOES NOT have VR/Hall sensor inputs. As these sensors are mandatory to operate an EMS there are pin headers/DIP8 socket and places for shunt resistors (used with VR) to be used with a separate BrickRPM VR conditioner board. More info at: http://brickems.com/brickrpm/

## Notes

The project uses a separate Molex connector library I found here:
https://code.google.com/p/rdubniewski-test/source/browse/trunk/eagle.lib/con-molex-5569.lbr

It's also included in the libs directory.

If you decide to home etch this pcb I recommend to make the vias larger (the copper area) before doing so. This way its easier to drill them and solder the connecting wire.

Heres a good tip for home made vias:
http://www.youritronics.com/double-layer-pcb-home-made-vias/

## TODO

* Clean up the messy looking schematic
* Get more testing done and lots of driving/racing.
* Possibly put a dual VR conditioner on board (MAX992x based)

## CPU Modules used with FreeEMS (MC9S12XDP512)

* **TA Adapt9S12XDP512** - http://www.technologicalarts.ca/shop/store/details/453/11/microcontrollers/adapt9s12xdp512m2-xgate-mcu-module,-full-configuration.html
* **ElMicro CardS12** - http://elmicro.com/en/cards12.html
* **WayEngineer MC9S12XDP512-core** - http://www.wayengineer.com/index.php?main_page=product_info&products_id=281
	