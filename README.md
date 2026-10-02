# Theory of operation:
* Power source is connected to USB1 (can be populated with USB-C or USB-A)
* USB2 can have its power turned on/off by the MCU using io12 (can be populated with USB-C male or female)
* LED1 is an RGB addressible LED for status indication
  * RGBW now... Austin's fault... Blame Austin
* SW1 is on io13 of the MCU and can be used for local control
* When using USB-C on both ends, CC1 & CC2 are pased through (but swapped) and should allow for USB-PD capabilities

# Notes:
* Overall board outline is non-negotiable unless it gets shorter!
* The curved lines on user.3 in the corners are there to indicate where the corners will be after applying "Shape Modification / Fillet Lines"
* Suspect it might be a good idea to include more of the custom symbols & footprints here in the repo... Working on it...

# Thoughts (now that there's a USB-C connector at each end...)
* CC1 & CC2
  * ATM, we simply pass them through (but swapped along the way for simplicity...)
  * Also: R9 & R10 are there to add 5k1 resistors if needed.
  *  Now the ESP handle them via io2...

# Power Monitoring thoughts
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
