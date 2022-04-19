# BTC-7A-Firmware-Images
This repository contains firmware images for BTC-7A Browning Trail Camera.

See the following posts for backround, context, and additional instruction:

- [IR to White Flash Trail Camera Conversion](https://winterberrywildlife.ouroneacrefarm.com/2021/09/15/ir-to-white-flash-trail-camera-conversion/)
- [Using a Trail Camera to Trigger a DSLR Camera](https://winterberrywildlife.ouroneacrefarm.com/2021/12/03/using-trail-camera-to-trigger-a-dslr-camera/)


The firmware images (named in the left column) are created with the following features/options enabled. 

| Image Directory | Battery Monitor | White-Flash | IR Filter | Custom Ribbon | Night Video Limit | Arm Delay | DSLR Trigger |
| ----------------| ----------------| ------------| --------- | ------------- | ----------------- | ----------- | ---
| [Baseline](https://github.com/robertzak133/BTC-7A-Firmware-Images/blob/main/Baseline/brnbtc70.BRN) |  standard         | no         | disengaged     |     no        | yes           |  30 Sec      | no |
| [CR_NV]()    |    standard        |   no        |  disengaged | yes         |      no           |  30 Sec    |   no      | 
| [WF_E_CR_NV](https://github.com/robertzak133/BTC-7A-Firmware-Images/blob/main/WF_E_CR_NV/brnbtc70.BRN) |  standard | yes        | engaged   |     yes       |  no           |  30 Sec | no |
| [WF_E_CR_NV_20S](https://github.com/robertzak133/BTC-7A-Firmware-Images/blob/main/WF_E_CR_NV_20S/brnbtc70.BRN)  |  standard | yes        | engaged   |     yes       |  no           |  20 Sec | no |
| [WF_D_CR_NV_20S](https://github.com/robertzak133/BTC-7A-Firmware-Images/blob/main/WF_D_CR_NV_20S/brnbtc70.BRN)     |  standard | yes        | disengaged|     yes       |  no           |  20 Sec | no |
| [CR_NV_DSLR](https://github.com/robertzak133/BTC-7A-Firmware-Images/blob/main/CR_NV_DSLR/brnbtc70.BRN)            |  standard |no         | disengaged        |     yes       |  no           |  30 Sec | yes |
| [WF_E_CR_NV_DSLR](https://github.com/robertzak133/BTC-7A-Firmware-Images/blob/main/WF_E_CR_NV_DSLR/brnbtc70.BRN) | standard | yes            | engaged   |  yes   |  no | 30 Sec | yes |
| [BM_WF_E_CR_NV](https://github.com/robertzak133/BTC-7A-Firmware-Images/blob/main/BM_WF_E_CR_NV/brnbtc70.BRN) | stateful  | yes            | engaged   |  yes   | no  | 30 Sec | no |
| [BM_WF_E_CR_NV_DSLR](https://github.com/robertzak133/BTC-7A-Firmware-Images/blob/main/BM_WF_E_CR_NV_DSLR/brnbtc70.BRN) | stateful  | yes            | engaged   |  yes   | no  | 30 Sec | yes |


* Image Directory: Directory and link in GitHub Site where image, in a file named brnbtc70.BNR can be found
* Battery Monitor: "standard" is factory default based on voltage measurement.   "stateful" tracks the amount of energy used and subtracts this from the energy available in a fully charged battey pack.  Battery monitor is in alpha state. 
* White-Flash: Supports white flash conversion
* IR Filter: Whether IR filter is engaged at night (default), or disengaged.  For White Flash options, the position of the IR filter has a small effect on the white balance of the resulting photos/videos.  "Engaged" produces a slightly blue-tinged image; whereas disengaged a slightly yellow-tinged image.  
* Custom Ribbon: In "Playback" menu, the date and time of the photo/video are shown is larger font at the bottom of the playback screen, making it easier to tell when the image was taken when reviewing in the field. 
* Night Video Limit: The default manufacturer firmware limits night time (flash illuminated) videos to 20 Seconds.  This option removes that limit, allowing illuminated videos of the same duration as daylight videos.
* Arm Delay: the default manufacturer arms the camera after 30 second.  This option reduces the arm time to 20 seconds.
* DSLR Trigger: Causes the "aim led" to turn on whenever a photo or video is taken.  This LED can be used to trigger a DSLR camera, while also allowing the trail camera to take photos or video.


## Download Instructions
- Find the copy of brnbtc70.BRN file you're interested in one of the folders here
- Click on it; then press "Download"
- Copy this file onto an SD card at the "top level" (not into a folder on SD card).  You can do this without physically swapping SD card around by plugging the BTC-7A into a USB port on your computer, and copying the brnbtc70.BRN file into the folder which appears with the camera
- Note -- the file must be named "brnbtc70.BRN".  Sometimes downloading from your browser will add extra characters to distinguish it from previous downloads -- e.g. "brnbtc70(1).BRN".  If this happens, rename file to "brnbtc70.BRN" on the SD card. 

## FW install Instructions

Before installing new firmwarwe, make sure you have batteries that will easily power the camera for the several minutes it takes for firmware upgrade. Losing power during firmware upgrade is bad, requiring that the camera be reprogrammed by the manufacturer.  

On BTC-7A
- Press "Mode" button 
- Select "CAMERA SETUP"
- Select "FW UPGRADE"
- Select "YES"

Display should show "UPGRADING".  For BASELINE image, this should take about 20 seoconds; for other images it can take 2-3 minutes; DO NOT TURN OFF OR REMOVE BATTERIES DURING THIS TIME! (this will "brick" the camera).  

Camera will then "Reboot" with new firmware.

Note that updating firmware resets the camera configuration settings, including the date and time. 
