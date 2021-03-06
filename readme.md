These Bluetooth examples show how to create a heart monitor and heather temperature measurement sensor. For the pulse sensor you will need a heart rate sensor from pulsesensor.com. 

For the temperature measurement example you will need a grove temperature sensor or use any of the readily available sensors and adjust the temperature reading code - we left it mocked up so you can get a value out without a sensor attached. 

In both cases useful we used the nrfToolbox app for Ios and Android to collect the data. You will also find nrfConnect and LightBlue very useful apps to see the raw services, characteristics and data.

The important part of both examples is the demonstration of bluetooth service and characteristic creation which is at the heart of bluetooth. A couple of other important things to note. One is that the bluetooth stack is large and so we cut the size of the spiffs partition in using an NTP server to get the time (so we need WiFi too). PlatformIO makes it easy to do so in the platformio.ini file. 

The other thing to note is that in both cases we use two timers so as not to affect the measurement acquisition. Well, at least minimize it. If you start adding "delay"s you'll affect the heartbeat readings for example. Not so critical in the  case of the temperature sensor. 

These two examples should give you a framework for developing your own Bluetooth device.

