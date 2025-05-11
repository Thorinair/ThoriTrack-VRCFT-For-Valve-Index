# ThoriTrack - Assembly Guide

Below is an assembly guide for building your own ThoriTrack. Pay close attention to all steps as some might be important.

## 1. Part Acquisition

Navigate back to the root of the repository and buy all of the parts listed in the [Hardware](../README.md#hardware) section. All parts are important unless listed as optional. Feel free to get the screws wherever is easiest, maybe at a local construction store, or from AliExpress or some other website.

## 2. Part Printing

This build has many different 3D printed parts. Print them according to the [3D Printable Files](../stl) document. Pay attention to the settings!

## 3. Firmware Flashing

First prepare the ESPs with the cameras. You want to use the camera cable extender cables as well as the extender sockets that you previously bought. These are all needed so that the cable can reach the lens of the Index. You can use the [Official Guide](https://docs.eyetrackvr.dev/how_to_build/preparing_xiao) to get the general idea for assembly. The final should look like on the image below. You will be running in wired mode.

![Assembly 01](img/01.jpg?raw=true)

Once assembled like this, flash firmware on both of them. You can follow the [Official Guide](https://docs.eyetrackvr.dev/firmware_guide/flashing_tool) in order to do this. Check if the output works via COM ports in the official ETVR app before continuing.

## 4. Camera Focusing

This is a good time to focus the cameras, as it will be difficult later on. ThoriTrack holds cameras by their lens so you cannot focus them afterwards. To focus the cameras, find some small piece of text that you can use. Think of it like an eye test. Grip the camera by the base with a tool like pliers, and grip the lens with another pliers. Carefully twist until the glue gives way.

Afterwards, you can focus by hand. Below is an example for the focusing procedure. You can use the ETVR app to monitor what the camera is seeing.

![Assembly 02](img/02.jpg?raw=true)

To get a better preview of the camera, grab one of the printed `EyeRing_Top_L` lens parts and insert the camera into it like on the image below. Then bring it close to your eye as if it was the lens of your Index. Use this as the proper focusing image and make any adjustments until you get a clear image. Repeat this process for both cameras to get good clear image.

![Assembly 03](img/03.jpg?raw=true)

![Assembly 04](img/04.jpg?raw=true)

## 4. Building The Eye Tracking Assembly

This is the main assembly that goes on the front of the headset. We will build it first.

Begin by soldering together the V4 Lite board. Follow the [Official Guide](https://docs.eyetrackvr.dev/how_to_build/led_setup#wiring-up-v4-lite) for this. You want to use the resistor for Dual Eye setup. In addition to the guide, also solder in 3 sets of 2x1 header pins. This will allow you to unplug stuff easier.

![Assembly 05](img/05.jpg?raw=true)

Now take off the camera hat from **one** of the ESPs and solder in 2 wires for powering the V4 Lite board. Red into VUSB, black into GND. Crimp together a 1x2 female dupont connector for easier unplugging. Cut off any excess solder on the bottom of the ESP so that it is flush. It should look exactly like on the image below once done. Once done, return the hat onto the ESP.

![Assembly 06](img/06.jpg?raw=true)

We will now do the worst part, and that is assembling the LEDs. You want to create a chain of them like shown on the images below. You can use the two `EyeRing_Bottom_L` and `EyeRing_Bottom_R` printed parts as a guideline for how long the cables should be. When soldering, always solder on the side of the PCBs where there is no LED. Don't push the wires through the holes, as the remaining solder could impede construction of the rings. **The long wire needs to be around 36cm in length.** In general, follow the image below to see exactly how to do it. Finally, crimp 1x2 dupont female connectors to the end of the long wires.

![Assembly 07](img/07.jpg?raw=true)

![Assembly 08](img/08.jpg?raw=true)

Test the assemblies to see if they work. Plug the ESP with the soldered wire into the V4 Lite board, as well as the 2 LED wires. **MIND THE POLARITY.** Polarity is marked on the V4 Lite board, or just have a look at the image below. Once plugged in, use the camera feed to verify that all of the LEDs work.

![Assembly 09](img/09.jpg?raw=true)

![Assembly 10](img/10.jpg?raw=true)

Unplug all of the wires from the V4 Lite board and tighten it into the `ETVR_Cradle` printed part using the M2*5 Counter Sunk Self-Tapping Screw.

![Assembly 11](img/11.jpg?raw=true)

Thread the two ESPs through the `ETVR_Holder` printed part and lay them into the `ETVR_Cradle`. The camera wires may provide some resistance and it could be a bit annoying to keep them still.

![Assembly 12](img/12.jpg?raw=true)

Place the `ETVR_Holder` over the ESPs and tighten it using 4x M3*10 Hex Head Screws. Most screws in this build are screwed directly into the plastic. So if it is not going, just push onto the screw until it catches the plastic.

![Assembly 13](img/13.jpg?raw=true)

Place the previously soldered LEDs and the camera into their correct slots on the `EyeRing_Bottom_L` and `EyeRing_Bottom_R` printed parts. Should look like on the image below. Make sure to also pull the camera through before that, or you will need to remove the LEDs later. Do this for both eyes. When looking at the previous picture, left eye will be on the right from you, and right eye will be on the left, because the camera cables go over above the headset.

![Assembly 14](img/14.jpg?raw=true)

Place the `EyeRing_Top_L` and `EyeRing_Top_R` printed parts over the bottom ones, effectively covering the LEDs. This serves as a holding system instead of using hotglue or some other type of glue. Secure each of the rings with 2x M2*6 Hex Head Screw and 1x M2x8 Hex Head Screw. Use the longer screw with the hole closest to the camera. Tighten the screws slowly and carefully so that the rings dont bind or break. These are small and fragile parts.

![Assembly 15](img/15.jpg?raw=true)

Place the cameras into the round half-slots and tighten them using the `EyeRing_Camera` printed parts. There is one for each eye. Use 2x M2*6 Hex Head Screw to tighten. The final eyering assembly should look like on the image below. Do this for both left and right eyes.

![Assembly 16](img/16.jpg?raw=true)

Lay the two eyerings out on your work area and make note of how the camera cables are twisted in the image below. Make sure that they aren't tangled or anything like that. Plug in the LED wires into the V4 Lite board again. For convenience, the printed part also has small + symbols on it for wire orientation.

![Assembly 17](img/17.jpg?raw=true)

Turn the eye rings around and use electrical tape to tape the LED wires with the camera cables. You can do it every few stops in order to secure them. THe result should be like on the image below. Make note of how the wires are threaded in relation to the camera cables, as well as how the camera cable is not twisted.

![Assembly 18](img/18.jpg?raw=true)

Tape the camera and LED wires up like on the image below. **Leave around 4cm of untaped cable** on the side where the extender is. I found that this is necessary otherwise the Index face gasket will not fit over them. On the other side, tape all the way to ESPs. Taping is important to keep the cables safe from damage. Use image below as a guide.

![Assembly 19](img/19.jpg?raw=true)

Finally, put the `Cover` printed file over the electronics and tighten it down using 3x M3*16 Hex Head Screws. Do this similar like previously with other screws.

![Assembly 20](img/20.jpg?raw=true)

The construction of the Eye Tracking Assembly is now complete! You can put it to the side while you prepare the Index itself for attaching this to it.

![Assembly 21](img/21.jpg?raw=true)

## 4. Building The Index Assembly

**TODO: Need to still write this guide!**