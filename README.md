# BTC-7A-Firmware-Images
This repository contains firmware images for BTC-7A Browning Trail Camera
These images include:
- /Manufacturer-Baseline/ : FW consistent with manufacturer install; revert to this as necessay
- /White-Flash-Custom-Ribbon/ : FW that supports White Flash conversion; as a bonus, also includes large (readable) date/time at the bottom of the screen during photo/video playback; removes limitation of 20 seconds for night time video

## Download Instructions
- Find the copy of brnbtc70.BRN file you're interested in one of the folders here
- Click on it; then press "Download"
- Copy this file onto an SD card at the "top level" (not into a folder on SD card).  You can do this without physically swapping SD card around by plugging the BTC-7A into a USB port on your computer, and copying the brnbtc70.BRN file into the folder which appears with the camera
- Note -- the file must be named "brnbtc70.BRN".  Sometimes downloading from your browser will add extra characters to distinguish it from previous downloads -- e.g. "brnbtc70(1).BRN".  If this happens, rename file to "brnbtc70.BRN" on the SD card. 

## FW install Instructions

Before installing new firmwarwe, make sure you have batteries that will easily power the camera for the several minutes it takes for firmware upgrade. Losing power during firmware upgrade is bad, requiring that it be reprogrammed by the manufacturer.  

On BTC-7A
- Press "Mode" 
- Select "CAMERA SETUP"
- Select "FW UPGRADE"
- Select "YES"

Display should show "UPGRADING" for about 2-minutes; DO NOT TURN OFF OR REMOVE BATTERIES DURING THIS TIME! (this will "brick" the camera).  Camera will then "Reboot" with new firmware.
Note that updating firmware resets the camera configuration settings, including the date and time. 
