# teensyknot

An modern high-precision implementation of a low-accuracy 16th century boat speed measuring tool.

Count (literal) knots on a [chip log](https://en.wikipedia.org/wiki/Chip_log) with a Teensy dev board and broadcast them on a NMEA-2000 network.

# Introduction

The "knot" is a measure of speed equal to 1 nautical mile per hour.  A nautical mile used to be defined as 1 minute of travel, but then someone
figured out the planet wasn't a perfect frictionless sphere (meaning a minute wasn't the same distance at all places on the planet, see 
[History of Geodesy](https://en.wikipedia.org/wiki/History_of_geodesy)), so we've settled on 1,852 metres as a standardize unit.  
1 knot is 1852 meters per hour.

# Supplies you'll need

1. [A Teensy board with a NMEA-2000 connector](https://copperhilltech.com/teensy-4-0-with-nmea-2000-connector-and-240-x-240-ips-lcd/)
2. A roll of line [like this](https://www.defender.com/product3.jsp?path=-1&id=945169)
3. An accelerometer that can work with the Teensy [like this one](https://www.adafruit.com/product/2809)
4. Some misc bits of plastic or wood
5. A spool

Notes:
  - Get a line that floats
  - Make sure the line will be strong enough to haul in the log when you're done

# Theory of operation

1. Throw the "log" in the water.  It'll drag behind the boat and un-reel the line as you sail away from it.
2. Knots tied in the rope will "bump" the accelerometer and allow the Teensy to measure how far the line has played out.
3. The Teensy will calculate speed and broadcast on the NMEA-2000 network it's attached to.
