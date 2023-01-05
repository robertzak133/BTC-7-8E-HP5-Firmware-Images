# BTC-7-8-E-HP5-Firmware-Images
This repository contains firmware images for BTC-7E-HP5 and BTC-8E-HP5 Browning Trail Cameras.

There was a bug in the firmware labeled "WWL7EH5_221210A" (for the 7E-HP5) and "WWL8EH5_221210A" (for the 8E-HP5) which prevents new firmware from being loaded.  This was caused by a new data structure in the menu system which I did not realize had to be terminated by a null entry.  Firmware versions "WWL7EH5_230104A" (for the 7E-HP5) and "WWL8E5H_230104A" (for the 8E-HP5) fix this problem.  Unfortunately, I do not know of a workaround for the earlier bug.  If you installed the buggy version in your camera, and now would like to load new firmware, please let me know in comments/issues below. I have a possible plan.

See the following posts for backround, context, and additional documentation:
- [New Optional Features for Browning HP5 Trail Camears](https://winterberrywildlife.ouroneacrefarm.com/2022/12/19/new-optional-features-for-browning-hp5-trail-cameras/)

- [Adding Features to Browning Elite HP5 Firmware](https://winterberrywildlife.ouroneacrefarm.com/2022/11/14/adding-features-to-browning-elite-hp5-firmware/)

- [Using a Trail Camera to Trigger a DSLR Camera](https://winterberrywildlife.ouroneacrefarm.com/2021/12/03/using-trail-camera-to-trigger-a-dslr-camera/)



| BTC-7E-HP5      | BTC-8E-HP5     | Bundle A    | 
| ----------------| ---------------| ------------|
| [Baseline](https://github.com/robertzak133/BTC-7-8E-HP5-Firmware-Images/tree/main/BTC-7E-HP5-Firmware-Images/Baseline)    | [Baseline](https://github.com/robertzak133/BTC-7-8E-HP5-Firmware-Images/tree/main/BTC-8E-HP5-Firmware-Images/Baseline)   |  no         | 
| [BA](https://github.com/robertzak133/BTC-7-8E-HP5-Firmware-Images/tree/main/BTC-7E-HP5-Firmware-Images/BA)          | [BA](https://github.com/robertzak133/BTC-7-8E-HP5-Firmware-Images/tree/main/BTC-8E-HP5-Firmware-Images/BA)         | yes         |


* BTC-7e-HP5: Directory in GitHub Site where image for BTC-7E-HP5 can be found
* BTC-8e-HP5: Directory in GitHub Site where image for BTC-8E-HP5 can be found
* BA (Bundle A) : A set of customizations aimed at improving overall camera usability 
 * Custom Ribbon: In "Playback" menu, the date and time of the photo/video are shown is larger font at the bottom of the playback screen, making it easier to tell when the image was taken when reviewing in the field.
 * Night Video Limit: The default manufacturer firmware limits night time (flash illuminated) videos to 20 Seconds.  This option removes that limit, allowing illuminated videos of the same duration as daylight videos.
 * Custom Info Strip: Adds "seconds" to the time of day; adds battery percent; compresses the size of the browning logo so it doesn't extend up into the main screen space.
 * Custom Volume/Directory/Filenames: Normally, this camera renames the SD card "volume"  to "BROWNING", in folders in DCIM called xxxBTCF, in files called IMG_xxxx.  With this modification, these labels are all taken from the camera name, as set by the user.  Note that only the first 5 and 4 characters are used for the folder and file suffix/prefix respectively.  Thus, for camera name, "MYCAMERA", the SD card will be labeled "MYCAMERA" and files can be found in DCIM/100MYCAME/MYCA0001.JPG.  Any "space" in the first 5 characters is replaced by an "underscore".
 * Customizable Date/Time Formats: New menu selections allow you to choose date (MM/DD/YYYY, DD/MM/YYYY, YYYYMMDD) and time (12-hour, 24-hour) formats used on infostrip and during "custom ribbon" during Playback.  
 * DSLR Trigger: Causes the "aim led" to turn on whenever a photo or video is taken.  This LED can be used to trigger a DSLR camera, while also allowing the trail camera to take photos or video. Selectable with new menu item
 * Extended SD Power: Causes the CPU and SD card to remain powered on for 30 seconds after each photo or video.  This to allow shared SD card to be read by another device.  Note that during this time, the camera will not trigger.  Selectable with new menu item. 


## Download Instructions
- Find the copy of brnbtc72.BRN (BTC-7E-HP5) or brnbtc82.BRN (BTC-8E-HP5) file you're interested in one of the folders here
- Click on it; then press "Download"
- Copy this file onto an SD card at the "top level" (not into a folder on SD card).  
- Note -- the file must be named "brnbtc72.BRN" (for BTC-7E-HP5) or "brnbtc82.BRN" (for the BTC-8E-HP5).  Sometimes downloading from your browser will add extra characters to distinguish it from previous downloads -- e.g. "brnbtc72(1).BRN".  If this happens, rename file to "brnbtc72.BRN" (or "brnbtc82.BRN") on the SD card. 

## FW install Instructions

Before installing new firmware, make sure you have batteries that will easily power the camera for the several minutes it takes for firmware upgrade. Losing power during firmware upgrade is bad, requiring that the camera be reprogrammed by the manufacturer.  

On BTC-7E-HP5 or BTC-8E-HP5
- Press "Mode" button 
- Select "CAMERA SETUP"
- Select "FW UPGRADE"
- Select "YES"

Display should show "UPGRADING".  Loading the firmware should take about 20 seoconds. DO NOT TURN OFF OR REMOVE BATTERIES DURING THIS TIME! (this will "brick" the camera).  

Camera will then "Reboot" with new firmware.

Note that updating firmware resets the camera configuration settings, including the date and time. 

## Reinstalling Factory Firmware
If, for any reason, you want to get back to the factory firmware, choose the "Baseline" entry in the table above to get the baseline factory image, and install that
