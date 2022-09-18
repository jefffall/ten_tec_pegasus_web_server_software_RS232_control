This software is used to control a Ten Ten Pegasus via a web browser.

The software will interface via an RS232 USB cable to the Pegasus from an iMac or Apple MacBook Pro.
This software is NOT Tested on Microsoft Windows.

It will run on MacOS Big Sur or most newer MacOS systems.

Requirements:

1) Install python3 on the iMac or Macbook.
2) you will need pip3 to be installed.
3) Use pip3 to install flask as: pip3 install flask

Use the file named pegasus to start the program running on your imac or Macbook AFTER the USBFDDI cable is connected to the Ten Tec Pagasus.

Put the file called pegasus into your /usr/local/bin

Here is hte contents of the pegasus script file:

jfall@Jeffreys-MacBook bin % more pegasus
#!/bin/bash
python3 /Users/jfall/eclipse-workspace/ten_tec_Pegasus_serial/src/pegasus_flask.py /dev/cu.usbserial-AQ00T6NF

Change the above line to MATCH YOUR directory structure. Fill in the /dev/cu.??? to be the unique ID of your USB cable
in /dev on your iMac or MacBook.

You can simply use your name as the ?Users/Yourname and change teh directory structure.

When you do a git clone you can match the file above to your directory structure.

then type in pegasus

The program should load pegasus_flask.py and this wil force u a Safari browser as:

localhost:8080

And you will see the pegasus webpage with band selection.

Note:
you will need the Ten Tec 302 encoder and cable to attach to the Pegasus
and then turn the encoder knob to changge frequency.

You will then see hte frequency change on the webpage.

You can use the 302 encodeer to change the volume and the filter width.
Or you can use the drop downs.


You will need to use pip3 to install ANY python3 modules which are missing.

Here are the imports:

import threading
import time
import struct
import webbrowser
import urllib3


from flask import Flask, request, jsonify

Python will try to load these. If any are missing on your system then as root

pip3 install flask

and anything else missing use pip3 to install it.

That should be about it.

search eBay for the cable with this string:

FTDI USB Cat/Programming cable TenTec Jupiter Argonaut V Orion Pegasus Omni VII

This is the USB Cable you will need to plug into yoir iMac or Macbook and the other end into the Ten Tec Pegasus.

Then look in /dev for the name of the cable
and then alter the name in the pegasus script.

that's it.
Have fun

 
