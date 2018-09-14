# MiniBadge2018

Based on the minibadge by luke jenkins: https://github.com/lukejenkins/minibadge


Kicad files in the Minibadge folder.

I have never made a pcb or a schematic before so if it is flawed greatly then I apologize.  The minibadge receives power from the badge and uses an ATTiny85 to control the LEDs. I wanted to do something with IC2 but this is a new hobby and I didn't know what I was doing. 

The ATTiny85 will need to be programmed first. I used a Arduino MEGA 2560 but a UNO can be used. The ArduinoISP program that can be found in Examples didn't work for me and I found the following code to turn the Arduino into an ISP: 

https://github.com/adafruit/ArduinoISP/blob/master/ArduinoISP.ino

Load ArduinoISP onto the MEGA.

Add https://raw.githubusercontent.com/damellis/attiny/ide-1.6.x-boards-manager/package_damellis_attiny_index.json into Additional Boards Manager URLs and then add the attiny board.

With your MEGA still connected select ATTiny25/45/85 and select Processor ATTINY85.

Connect the following between the header on the minibadge and the MEGA:

Mini		MEGA

GND	-	GND
5V 	-	5V
MISO	-	50
MOSI	-	51
CS	-	53
SCK	-	52

Connect a 10uf capacitor between RESET and GND on the MEGA.

Select code and upload.

ATTiny Pins -

Pins 5, 4, and 3 control the LEDs.
