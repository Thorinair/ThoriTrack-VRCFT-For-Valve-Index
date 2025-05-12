# ThoriTrack - VRCFT For Valve Index

ThoriTrack is a mounting solution designed by Thorinair for mounting EyeTrackVR related hardware, and HTC Vive Facial Tracker to the Valve Index. Primary goal of the design is to make it more robust and "industrial" compared to other mounts without having to modify anything on the Valve Index.

![Overview Front](img/Overview-Front.jpg?raw=true)
![Overview Lens](img/Overview-Lens.jpg?raw=true)

This repository provides the STL files for 3D printing out your own ThoriTrack, as well as source blend files.

## Assembly Guide

You can read the assembly guide here: [ThoriTrack - Assembly Guide](guide/README.md)

## Folders

* `blend` - Contains source Blender files for the mount.
* `stl` - Contains printable STL files and instructions on how to print them.

## Hardware:

**Electronics:**

* 1x HTC Vive Facial Tracker
* 1x EyeTrackVR V4 Lite DIY LED Kit - [EyeTrackVR Store](https://store.eyetrackvr.dev/products/v4-1-lite-diy-led-kit)
* 1x USB A to USB-C - [Amazon](https://www.amazon.de/dp/B0B5WQW3LD?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1)
* 1x USB Hub with MTT - [Amazon](https://www.amazon.de/dp/B07YN54Q33?ref=ppx_yo2ov_dt_b_fed_asin_title)
* 2x USB-C to USB-C cable - [Amazon](https://www.amazon.de/dp/B09C2D9Z7T?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1)
* 2x XIAO ESP32S3 Sense boards - [AliExpress](https://www.aliexpress.com/item/1005004788285643.html?spm=a2g0o.order_list.order_list_main.335.27e01802Ww8woQ)
* 2x 75MM-160 850nm OV2640 Camera - [AliExpress](https://www.aliexpress.com/item/1005003040149873.html?spm=a2g0o.order_list.order_list_main.340.27e01802Ww8woQ)
* 2x 200mm A, 24p 0.5mm pitch Camera Extension Cable - [AliExpress](https://www.aliexpress.com/item/4000022157163.html?spm=a2g0o.order_detail.order_detail_item.5.3bfbf19cXqxT1M)
* 2x Flat Cable Extension Connector - [AliExpress](https://www.aliexpress.com/item/1005004283030442.html?spm=a2g0o.order_list.order_list_main.324.27e01802Ww8woQ)

**Screws:**

* 1x M2*5 Counter Sunk Self-Tapping Screw
* 8x M2*6 Hex Head Screw
* 2x M2x8 Hex Head Screw
* 2x M3*8 Hex Head Screw
* 8x M3*10 Hex Head Screw
* 3x M3*16 Hex Head Screw
* 4x M3*20 Hex Head Screw
* 2x M3*10 Counter Sunk Screw
* 2x M4*20 Counter Sunk Screw
* 2x M3 Nut
* 2x M4 Lock Nut

**Extras:**

* Double sided tape
* 3x Male 1x2 Header Connectors
* 3x Female 1x2 Dupont Connectors
* Black Insulation Tape
* Wires for wiring it up
* (Optional) 2x 8.8x8.8x5mm Aluminum Heatsinks [AliExpress](https://www.aliexpress.com/item/1005004079109702.html?spm=a2g0o.order_list.order_list_main.11.5b9a1802sGerX3)

## Recommended Software:

* Eye Tracking: [Ryan9411's ML based Eye Tracking](https://github.com/ryan9411vr/EyeTracking)
* Face Tracking: [Vive SRanipal Software (VRCFT Docs Page)](https://docs.vrcft.io/docs/hardware/addons/vive/face-tracker)


## Credits

* Bottom part of the eye ring is based on the [Phys-Index-EyetrackVR-HW](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW) eye rings, with one of the LEDs moved away from the nose, as well as the camera mount removed.
* The HTC Vive Facial Tracker arm is based on the ["Road to Alcoholism"](https://docs.vrcft.io/docs/hardware/addons/vive/face-tracker#valve-index) design, with the arm slightly lengthened and changed around to support nuts and screws.