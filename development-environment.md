# Development Environment Notes

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

How do I get access to that file system from my bash shell?
