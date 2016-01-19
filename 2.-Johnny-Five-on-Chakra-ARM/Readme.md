# Step 2
## Get Johnny-Five working on a Raspberry Pi in Windows with Arduino

This will build upon [Step 1](https://github.com/BrianGenisio/win-io/tree/master/1.-Johnny-Five-on-Chakra-x86).  Instead of running on a PC (or VM), run on Chakra ARM directly on the Raspberry Pi.

### Notes
- Try to use  [this workflow](https://ms-iot.github.io/content/en-US/win10/samples/NodejsCylon.htm).  I think it will be much more rapid than developing in Visual Studio and sending the package over every time.  It will mount the Pi drive on the dev box, and run node from remote shell.
- Microsoft put out an example of [using Johnny-Five on IoT](http://ms-iot.github.io/content/en-US/win10/samples/NodejsWUJ5.htm).  I still think the above workflow is better than using Visual Studio to publish, but knowing that J5 works now on IoT is a huge plus.  I'd still like to put it through its paces to make sure that there are no other gotchas.

### Platforms
- [ ] Arduino
- [ ] Particle
- [ ] Imp

### Devices
- [ ] LED
- [ ] Sensor
- [ ] Servo
- [ ] Motor
- [ ] Temperature
- [ ] Accelerometer
- [ ] I2C Devices?
