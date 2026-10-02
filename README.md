# Theory of operation:
* Power source is connected to USB1
  * can be populated with USB-C female or USB-A male
* USB2 can have its power turned on/off by the MCU using io12
  * can be populated with USB-C male or female
* LED1 is an RGB addressible LED for status indication
  * RGBW now... Austin's fault... Blame Austin
* SW1 is on io13 of the MCU and can be used for local control
* When using USB-C on both ends, CC1 & CC2 are pased through (but swapped) and should allow for USB-PD capabilities
  * Also: R9 & R10 are there to add 5k1 resistors if needed.
    * Now the ESP handles inserting them via io2...

![A 3D render of the device](/Pix/TinkerLink top.png)
# Power Monitoring thoughts:
* INA chip selection
* The following are all drop-in replacements for each other...
  * INA228 (Current chip in the design)
    * very expensive
    * 625uA resoluation
  * INA237
    * 1/3 the price
    * 800uA resoluation
  * INA226
    * under a buck...
    * 1.5mA resoluation

# Firmware:
* Yet to be developped...
* Might work with TasmOTA like the original SiniLink could
