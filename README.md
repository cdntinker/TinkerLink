# Theory of operation:
* Power source is connected to USB1 (can be populated with USB-C or USB-A)
* USB2 can have its power turned on/off by the MCU (can be populated with USB-C male or female)
* LED1 is an RGB addressible LED for status indication
* SW1 is on io4 of the MCU and can be used for local control
* When using USB-C on both ends, CC1 & CC2 are pased through (but swapped) and should allow for USB-PD capabilities

# Notes:
* Overall board outline is non-negotiable unless it gets shorter!
* The curved lines on user.3 in the corners are there to indicate where the corners will be after applying "Shape Modification / Fillet Lines"

# Thoughts (now that there's a USB-C connector at each end...)
* CC1 & CC2
  * Pass them through?
  * Maybe have the ESP handle them...
