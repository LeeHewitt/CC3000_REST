# CC3000_REST

## Overview

A simple REST API for Arduino and the CC3000 WiFi chip. It allows to make REST calls from a web browser or a webserver to control the pins of an Arduino board.

## Supported hardware

The library is at the moment compatible with the following Arduino boards: Uno, Mega, Due, Teensy 3.0.

It is also compatible with most CC3000 breakout board, and was tested with the Adafruit CC3000 breakout board and CC3000 WiFi shield.

## Quick test

1. Connect a LED & resistor to pin number 8 of your Arduino board
2. Open the sketch and modify the WiFi SSID, password & security
3. Upload the sketch
4. Go to a web browser and type arduino.local/mode/8/o to set the pin as an output
5. Now type arduino.local/digital/8/1 and the LED should turn on

## API documentation

The API currently supports three type of commands: digital, analog, and mode.

Digital is to write or read on digital pins on the Arduino

Analog is to write or read on analog pins on the Arduino

Mode is to change the mode on a pin. For example:
  * /mode/8/o sets pin number 8 as an output
  * /mode/8/i sets pin number 8 as an input
