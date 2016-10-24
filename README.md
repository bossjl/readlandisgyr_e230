# readlandisgyr_e230
Read the counter data from a Landis Gyr E230 enery meter from Creos in 

You need:

  1) Raspberry pi, or another linux hardware with a free usb connector
  
  2) USB IR Interface, can be build on your own, but i just bought this one:
    http://shop.weidmann-elektronik.de/index.php?page=product&info=24
  
  3) Volkszaehler software (open source)
    http://www.volkszähler.org/

Part 1 - Volkszaehler: 

  Install the Volkszaehler frontent and middleware on a distinct server or on the raspberry

Part 2 - Raspberry  

  The USB IR interface should be detected as a tty device.
  Sadly, the vzlogger daemon (part of the Volkszaehler package, normally to be installed on the raspberry), which should normally read the OBIS data from the Energy Meter does not understand the Landis & Gyr OBIS Dialect, so i had the write my own reader.
  It's the file called readlandis.sh i this repo, the bash file also contains descriptive comments.
  
