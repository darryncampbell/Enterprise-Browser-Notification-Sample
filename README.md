# Enterprise Browser Notification Sample
Sample showing use of the Enterprise Browser [Notification](http://techdocs.zebra.com/enterprise-browser/latest/api/Notification/) and [MediaPlayer](http://techdocs.zebra.com/enterprise-browser/latest/api/mediaplayer/) APIs

Set-up
1. Install Enterprise Browser on your Android device and connect to adb
2. Run a local server (recommended) or copy the eb_notification.html file to the device
3. Modify the StartPage of Config.xml to point to eb_notification.html.  The Config.xml in this repository will assume a server running on 192.168.0.2:8001
4. Run the following commands:
  * adb push Config.xml /storage/emulated/0/EnterpriseBrowser/Config.xml
  * adb push claps.mp3 /sdcard/media/claps.mp3
  * adb push guitar.wav /sdcard/media/guitar.wav
5. Run Enterprise Browser on the device to view the test page which exercises the APIs.

**Note: The playFile method of the [Notification](http://techdocs.zebra.com/enterprise-browser/latest/api/Notification/) API is only designed to play media files from a folder from within the application's private data directory, not from somewhere like the mass storage directory**
