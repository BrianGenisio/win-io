# Development Environment Notes

## Getting the image written without a native Windows machine
I don't have a native Windows machine.  I have a Windows VM, but the tools they give don't allow you to write to your SD card.  I was successful by installing the OS package on my VM and copying the `flash.ffu` file to my Mac.  I had to use the [ffu2img utility](https://github.com/t0x0/random) to unpack it, but then I was able to do it:

0. Copy flash.ffu from Windows C:\Program Files (x86)\Microsoft IoT\FFU\RaspberryPi2\flash.ffu to the Mac
0. Convert the flash.ffu to an image: `python ffu2img.py /path/to/flash.ffu /output/path/rpi.win10.img`
0. Insert a class-10 SSD card into your Mac, and figure out the path to the SSD card: `diskutil list`
0. Unmount the SD card: `diskutil unmountDisk /dev/diskN` (replace N with the disk you found above)
0. Copy the IMG file to the SD card: `sudo dd bs=1m if=/path/to/rpi.win10.img of=/dev/diskN`
0. Wait a while (took me 1 hour).  When it is complete, put the SD card into the Raspberry Pi 2 and boot it up.

## Ethernet Sharing
Win 10 on Raspberry Pi only supports one WiFi adapter.  I'm not terribly interested in buying a $25 WiFi adapter for this, so I am using my Mac to share the internet connection:

System Preferences > Sharing > Internet Sharing
 - Share WiFi
 - USB Ethernet
 - Thunderbolt Ethernet
 
Then I plug an ethernet into my Mac and into the RPi.  When it boots, I get an IP of 192.168.2.2.  I'm not sure yet if that will be consistent.  I'd like to move this device to be headless.

## Connect vis SSH
```
bash > ssh Administrator@192.168.2.2
```

The default password is p@ssw0rd.  You can change it:
```
psh > net user Administrator [new password]
```

## Map the file system:
Finder > Go > Connect To Server 
Server Address: smb://192.168.2.2/C$

The file system is available from the command line at "/Volumes/C$"
