# Step 3
## Create the win-io adapter for native GPIO on Raspberry Pi

Once we know Johnny-Five works properly on ARM with an Arduino [(Step 2)](https://github.com/BrianGenisio/win-io/tree/master/2.-Johnny-Five-on-Chakra-ARM), create the win-io layer for Johnny-Five to access the GPIO on the Raspberry Pi.

### Notes
- The GPIO has already been [exposed by Microsoft](https://ms-iot.github.io/content/en-US/win10/samples/NodejsWUBlinky.htm).  This step might be pretty straight-forward.  More info on [MSDN](https://msdn.microsoft.com/en-us/library/windows.devices.gpio.aspx)
- Consider using [Board-IO](https://github.com/achingbrain/board-io) as a basis for the library.
- An overview of plugins can be found [here](https://github.com/rwaldron/io-plugins);

### Platforms
- [ ] Raspberry Pi

### Devices
- [ ] LED
- [ ] Sensor
- [ ] Servo
- [ ] Motor
- [ ] Temperature
- [ ] Accelerometer
- [ ] I2C Devices?
