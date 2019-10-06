A WIP attempt at making an OLED oscilloscope for Pure Data projects on BELA

Current demo uses a SSD1306 OLED Screen connected to a Bela Mini via I2C (p2.9 - SCL, p2.11 - SDA)
render.cpp looks for OSC messages coming from port 7562 with message "/param1".

The accompanying PD sketch is intended to be run on a PC connected to Bela via USB. Connect via the correct
IP address (prepopulated with 192.168.6.2, if you are on a mac you will need to change your address accordingly)
The sketch sends numeric float values from 0 to 1 based on an oscillator running at 10hz (the user
can manipulate the speed with the horizontal slider as well).

As the numeric values are received on the Bela side they are plotted from left to right. on the screen
once all pixels have been plotted from left to right the clear screen function is called and it starts
back at the left.
