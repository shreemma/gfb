# Introduction #

After dealing with loose dangly wires for so long I finally decided to design an Arduino OneWire Shield. It uses 4 pins, 2 for independent onewire networks, and two additional LEDs on the nice Tyco rj-45 connectors. Additionally I included space for the Dallas 3231 RTC which I sorely miss in most of my Arduino projects.

# Details #

Features:
  * 2 Independent OneWire RJ-45 ports with activity LED
  * 2 additional LEDs on the RJ-45 socket
  * Battery-backed RTC
  * 4 spots for local OneWire devices (2 on each network)

Parts:
  * 2x 1nF Cap
  * 2x 1uF Cap
  * CR1220 battery & holder
  * resistors for 1-wire network (4.7k-2.2k)
  * Dallas DS3231 RTC
  * 2x Tyco 1888250-1 RJ-45 socket
  * push-button for reset sw


## Want one? ##
I ordered the boards fabbed through seeedstudio (they are great!) and got the minimum 10 boards which obviously I don't need. Let me know If you need one and I'll send it your way for oh $10? (just the board) Does that sound reasonable? :)

http://lh5.ggpht.com/_IhezzMAaFLg/S_qaDs9QboI/AAAAAAAAGSg/yq6IwATng6Q/s720/IMG_0383.JPG
http://lh5.ggpht.com/_IhezzMAaFLg/S_qbMV1BSnI/AAAAAAAAGWw/sCSc_kHTOHk/s720/IMG_0392.JPG
http://lh6.ggpht.com/_IhezzMAaFLg/S_qbUJsnvII/AAAAAAAAGXI/jW1CqcBrsAU/s720/IMG_0393.JPG

## Update ##
As mentioned in the comments, there is a bug in this version of the board. You need to bridge a resistor to one of the OW ic spots to make it work. Unfortunately this uses up an OW spot on the board itself but other than that it's just a minor inconvenience.