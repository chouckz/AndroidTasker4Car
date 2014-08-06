AndroidTasker4Car
=================

Android Tasker scripts to use Android Tablet or other device as Car Media and Navigation center 

Android Tablet to replace car media and navigation system.
In Russian (http://habrahabr.ru/post/232357/)

This guide and Tasker script will help you to integrate Android Tablet in the car as very user friendly device.
- Activate and Standby you Tablet in proper way to save battery and avoid short term power glitches. 
- Resume your Song playing after Activation. Like normal Car Stereos.
- Switch between Media Payer and Navigation in one touch 
- Maximize usable screen area
- Control Media Player (Pause, Play, Next song etc) with one touch without leaving Navigation or other app 
- make Android to pronounce Artist and song title automatic on song change.
- Auto adjust screen brightness while driving

Demo Videos:
http://youtu.be/DbJmAnoYmbM
http://youtu.be/p-xeEB8NNVU
http://youtu.be/YBQvYkLJ05M 

0) The best candidate for it is Nexus 7, 1 gen. It is cheep, has enough CPU and convinient POGO PINS on Side. http://i47.tinypic.com/i4imx5.png . The only problem is absence of microSD , but you can do OTG and use any external storage.
1) First you need good 5v DC power supply. I suggest to get KIS3R33S based DC-DC module from eBay. It can convert 14v -> 5v with 2-3 Amp load.
2) Also you need audio input to your car amp. You can use Blue-tooth streaming or whirred AUX jack.
3) Next you need to decide on Audio Player. For a lot of reasons I suggest Google Music. But don't use latest version uninstall it with Titanium Backup and get v4.1.512 http://www.filedropper.com/tablet4car_1. I am old school and prefer to manage my play-lists remotely creating with .m3u files with WinAmp and upload them to the Tablet.
Google Music:
<img src="//habrastorage.org/files/a8c/0cc/e17/a8c0cce17474464fb05a4db24ff0e5fe.png"/>
<img src="//habrastorage.org/files/fd7/fed/ae0/fd7fedae04e44f7ea6acb2e2f58e08f0.png"/>
<img src="//habrastorage.org/files/77a/353/f75/77a353f75def4c6981f86712e75568c2.png"/>
4) Decide and get you navigation app. I prefer Garmin Navigon, for many reasons beside having Garmin HUD. 
<img src="//habrastorage.org/files/6c9/9f1/851/6c99f18510db45a5a6b44f8365513edf.png"/>

5) Install apps "Button Savior" and/or "full!screen". https://play.google.com/store/apps/details?id=de.tsorn.FullScreen&hl=en. I've made a custom version with custom icons fro NAV and Music  of Button Savior, http://www.filedropper.com/tablet4car_1 but when I found full!screen I switched to it. So you can skip Button Savior and use only full!screen. I still keep both.  <img src="//habrastorage.org/files/2c6/b33/4c8/2c6b334c82d54a4d9b4ec49badf48cf5.png"/>. Button Savior icons are on the right end of the screen. full!screen is a great app to allow two custom buttons in right and left bottom screen corners. You can set 3 actions on each of it (touch, long touch and swipe). You can set standard actions such  as Home, Menu, Back, or control Media Player (Pause, Play, Next song etc) or switch between apps like Alt+Tab in Windows.
<img src="//habrastorage.org/files/4d8/b3d/313/4d8b3d313f2444c88867fcdd130a6687.png"/>

6) However it is optional I suggest to use "Deep Sleep Battery Saver" to stop all unwanted activity (apps, GPS, WiFI, BT etc) on your tablet while car is off to save battery as it can consume 10-20% during one night and finaly run out of power in long idle.
<img src="//habrastorage.org/files/ae4/e5a/214/ae4e5a2145cc42bdb33dc8ac5c0078a6.png"/>
<img src="//habrastorage.org/files/4b9/345/b2a/4b9345b2ad7740959b65bcb0aba70cfe.png"/>

7) now we need "Lux+" app to Auto adjust screen brightness while driving. You can do the same with some custom ROMs. But is you on stock use this great tool.
<img src="//habrastorage.org/files/fbe/94c/d8e/fbe94cd8e46d4adbb437967486bd0f26.png"/>
<img src="//habrastorage.org/files/bda/e89/d38/bdae89d38e6f4980a84c20ad35c314aa.png"/>

8) To get better TTS I encourage you to use TTS iVona. it is free and much better then stock.

9) Now THE "Tasker" ! It is a great app ant if you not familiar with it pls read high level description to get idea what it is and what it can do. In two words it is custom scripting and triggering engine to do any automations with tonns of plug ins. Also I recommend to install "Secure Settings Pro" for it and "Secure Settings Helper". 
<img src="//habrastorage.org/files/1c2/45d/d2e/1c245dd2ed6c432f92df46ab10e575cc.png"/>
<img src="//habrastorage.org/files/d2f/df2/bbf/d2fdf2bbf1b64182bebe5cbcbb52e074.png"/>
<img src="//habrastorage.org/files/9e3/34f/332/9e334f332a5848518ae65f6cb64c993d.png"/>
<img src="//habrastorage.org/files/eca/5bc/d4d/eca5bcd4d2d54641865e65fb11027920.png"/>
10) Install Media Utilities plug-in to track and control Music Player activities from Tasker. It can get triggered when new Track  is started, get state (Play or Stopped) and Artist and Title for us to Say it with TTS. I supports not only Google Music, but most popular media players.
<img src="//habrastorage.org/files/28e/40b/8e1/28e40b8e11e24f319480c0a16c75f1a9.png"/>
11) For some procedures we will need TaskKill  plug-in, pls get it.
<img src="//habrastorage.org/files/f60/c57/3c9/f60c573c94a947bebdf8c00fe4609f6b.png"/>
12) Import(restore) and adapt my script for Tasker from https://github.com/chouckz/AndroidTasker4Car
<img src="//habrastorage.org/files/aa8/a11/41e/aa8a1141e0a047fa975569c9ec0b3bf5.png"/>
<img src="//habrastorage.org/files/d24/056/940/d240569407fe427484b3705eca304d1c.png"/>
<img src="//habrastorage.org/files/234/a19/d17/234a19d174514737aca226f01bdafc9c.png"/>
<img src="//habrastorage.org/files/eed/12f/dcb/eed12fdcb22a49d8861efa51d43a5a5a.png"/>

13) Tasker Profiles (triggers) description:
Power AC - Runs (DC ON, DC OFF) Tasks when power is supplied to the tablet. We assume that our Tablet is active only when it has DC power.
Media Utilities State New Track - Runs "Fill Track" task when new track is playing 
Media Utilities State Is Playing - Runs task "Now Playing" when music is playing and "Now Not Playing" when it stopped.
Device Boot - Runs task "Boot Startup" when tablet is started after complete power off or restart. May be useful when you shut-down tablet completely each time or in long cold winter.
Device Shutdown - Runs task "Shutdown" when tablet is shutting down.
Music - Runs task "Set Active App To Music" when Google Music is active (main app on the screen). Needed for Remote control only.
NAVIGON- Runs task "Set Active App To Navigation" when NAVIGON is active (main app on the screen). Needed for Remote control only.

For proper behaviour It is very important remove "Enforce Task Order" check box in all Profiles properties  <img src="//habrastorage.org/files/5e7/5f8/605/5e75f8605f2f47a896e170371967fc02.png"/>
If after booting you get warning "raise volume above safe level...." you can get read of it in system settings. If you can't do it there use this tool: http://forum.xda-developers.com/xposed/modules/mod-unsafe-volume-disable-safe-media-t2338474

14) Tasker Tasks(routines) description:
DC ON - Set variable %DCPOWER to 1, runs Lux Plug-in to start auto brightness and runs task "On".
DC OFF - Set variable  %DCPOWER to 0, and runs task "Off".
On - resumes Music Playing if it was stopped by short term power failure . Turns on GPS, WiFi, Bluetooth. Sets proper Volume.Say Voice greeting. Starts Music and Navigation apps (in case it they were killed while sleeping). If last time when car was stopped Music was playing Resume music and say title. Runs Lux Plug-in to start auto brightness.
Off - Stops Music . Turns off GPS, WiFi, Bluetooth. Kills Navigation app. Turns off screen. 
Resume Music - Prononce Artist and Title of audio track with proper TTS language. If you have two (like me you can set up it properly) in  Fill Track. Gently increase volume. 
Fill Track - Gets from "Media Utilities" Artist and Title of audio track , remembers them and determine proper TTS language to use. Also remembers last song artist so it wont pronounce it it it is the same as current. Pronounce Artist and Title of audio track.
Say Time - Fills current system time.
Now Playing - set %MPLAYING to 1. Music is Playing.
Now Not Playing - set %MPLAYING to 0. Music is not Playing.
Speed Volume Control Plus - looped automatic Volume control based on GPS speed and speed and 5 speed ranges with corresponding Volume set in Init Vars. This is like stock option in many car audio systems to increase Volume with the speed. To activate this task you need to run it from "On" Task and Stop it in "Off" task. This commands are there but disable. You need to Enable them.
Init Vars - Initialization os constants and variables.
Shutdown - runs "Off" Task

Next phase I will show how to control your tablet from Steering Wheel buttons.



