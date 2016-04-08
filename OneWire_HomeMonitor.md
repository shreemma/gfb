# Introduction #

A project to have arduino managed onewire thermometers around the house. Eventually I'll have a cron job to query the arduino nic (wiznet) and graph the data, but for now just stumbling through onewire network issues.

The data currently is being sent to [pachube](http://www.pachube.com) as a [feed](http://www.pachube.com/feeds/5916)!


# Details #

### Hardware: ###
  * [Arduino Duamillanove](http://arduino.cc/en/Main/ArduinoBoardDuemilanove) - Make sure to get the version with the Atmega328, the extra memory is required with later versions of the code.

  * [Adafruid etherShield](http://www.adafruit.com/index.php?main_page=product_info&cPath=17_21&products_id=83) - Well designed shield kits, make life easy :)

  * [WizNet WIZ811MJ Ethernet module](http://wiznet.co.kr/en) - Nothing special here, though I haven't used the other ethernet modules.

  * [Maxim-IC DS18B20, DS18S20, DS18B20P one-wire thermometers](http://www.maxim-ic.com/products/1-wire/) - Stick with the DS18B20 or DS18B20P version, the DS18S20 is not really worth the trouble.

  * [Maxim-IC DS2450 one-wire Quad A/D](http://www.maxim-ic.com/products/1-wire/) - Will be measuring voltages on my thermostat triggers to log when its heating/cooling. See my arduino library below.

  * [Hobby-Boards temp circuit boards](http://www.hobby-boards.com/catalog/product_info.php?cPath=25_28&products_id=48) - These are really nice though I wish they werent restricted to parasite power for the ds18's :(

  * [Hobby-Boards 6-Channel Hub](http://www.hobby-boards.com/catalog/product_info.php?cPath=23&products_id=1561) - Will probably be implementing this to simplify things a bit. Less messing with additional arduino pins... well, ok, not really sure why I bother :)

  * [Sparkfun 4x20 LCD w SerLCD backpack](http://www.sparkfun.com/commerce/product_info.php?products_id=462) - Pretty nice serial interface to the HD44780 on the lcd

  * Cat5e cabling in my walls...

### Software: ###
  * [Dallas Temp Library](http://milesburton.com/index.php?title=Dallas_Temperature_Control_Library), version 3.5 or newer.

  * [SparkFunSerLCD Library](http://www.arduino.cc/playground/Learning/SparkFunSerLCD)

  * [Ethernet2 Library](http://code.google.com/p/tinkerit/source/browse/#svn/trunk/Ethernet2) - This is older than the current arduino Ethernet library but seems to work better. Not sure whats going on here :(

  * [DS2450 library](http://code.google.com/p/gfb/source/browse/#svn/arduino/DS2450) - To use above Quad A/D with arduino.

  * [DS2409 library](http://code.google.com/p/gfb/source/browse/#svn/arduino/DS2409) - For one-wire switches similar to the [Hobby-Boards 6-Channel Hub](http://www.hobby-boards.com/catalog/product_info.php?cPath=23&products_id=1561)

# Notes #
  * Use a 2k2 Ohm resistor and NOT the 4k7 that Maxim suggests. 4k7 works on their master chips, but the ATmega328/168 requires less to do a proper pull-up. See pg321 of [ATmega328P Datasheet](http://www.atmel.com/dyn/resources/prod_documents/doc8161.pdf)
  * Serious nastyness going on in the arduino ethernet libraries. There is an older Ethernet2 library that includes some streamlined code and where the Server code works well but the client code has issues. On the other hand the more recent Ethernet code included with arduino-018 has updated client code but i cant seem to get the darned server code to work. Go figure. Solution? Run Ethernet2 as the base but copy over the client.h and client.cpp from the original lib. nas-ty!
  * For HVAC monitoring, you want to read +24 on Y for AC or +24 on W for heat.

# Thoughts #
Have been having some issues with DS18's not showing up on the network, or some of them wiping out the network entirely when plugged in. I think parasite power is partly to blame on the 30ft cat5 runs, but not really sure. I _really_ wish hobby-boards made a powered version of their board, I might try some of the other vendors to see if it makes a difference. Any thoughts or help is greatly appreciated. << This is just about resolved by knocking down that pull-up resistor to 2k2 and setting resolution to 9bits. I will be trying out a smaller resistor yet to see if it lets me increase the resolution.

# How it Looks #
http://lh4.ggpht.com/_IhezzMAaFLg/S3wKa_6kifI/AAAAAAAAFZs/2ZMVK3L_6qI/s640/IMG_0324.JPG
http://lh5.ggpht.com/_IhezzMAaFLg/S3wKoeintcI/AAAAAAAAFag/zH8cE_Ygv-8/s640/IMG_0326.JPG
http://lh3.ggpht.com/_IhezzMAaFLg/S3wKuIEyjLI/AAAAAAAAFbA/pwDlJKmLDWE/s512/IMG_0327.JPG
http://lh6.ggpht.com/_IhezzMAaFLg/S4HlKRz7DAI/AAAAAAAAFj0/6PY58eJPejU/s640/IMG_0332.JPG