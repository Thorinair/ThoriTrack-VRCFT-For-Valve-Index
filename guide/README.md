# ThoriTrack - Assembly Guide

Below is an assembly guide for building your own ThoriTrack. Pay close attention to all steps as some might be important.

## 1. Part Acquisition

Navigate back to the root of the repository and buy all of the parts listed in the [Hardware](../README.md#hardware) section. All parts are important unless listed as optional. Feel free to get the screws wherever is easiest, maybe at a local construction store, or from AliExpress or some other website.

## 2. Part Printing

This build has many different 3D printed parts. Print them according to the [3D Printable Files](../stl) document. Pay attention to the settings!

## 3. Firmware Flashing

First prepare the ESPs with the cameras. You want to use the camera extension cables as well as the extension connectors that you previously bought. These are all needed so that the cable can reach the lens of the Index. You can use the [Official Guide](https://docs.eyetrackvr.dev/how_to_build/preparing_xiao) to get the general idea for assembly. The final should look like on the image below. You will be running the ESPs in wired mode.

![Assembly 01](img/01.jpg?raw=true)

Once assembled like this, flash firmware on both of them. You can follow the [Official Guide](https://docs.eyetrackvr.dev/firmware_guide/flashing_tool) in order to do this. Check if the output works via COM ports in the official ETVR app before continuing.

## 4. Camera Focusing

This is a good time to focus the cameras, as it will be difficult later on. ThoriTrack holds cameras by their lens so you cannot focus them afterwards without releasing their clamps. To focus the cameras, find some small piece of text that you can use. Think of it like an eye test. Grip the camera by the base with a tool like pliers, and grip the lens with another set of pliers. Carefully twist until the glue gives way.

Afterwards, you can focus by hand. Below is an example for the focusing procedure. You can use the ETVR app to monitor what the camera is seeing.

![Assembly 02](img/02.jpg?raw=true)

To get a better preview of the camera, grab one of the printed `EyeRing_Top_L` lens parts and insert the camera into it like on the image below. Then bring it close to your eye as if it was the lens of your Index. Use this as the proper focusing image and make any adjustments until you get a clear image. Repeat this process for both cameras to get a good clear image.

![Assembly 03](img/03.jpg?raw=true)

![Assembly 04](img/04.jpg?raw=true)

## 4. Building The Eye Tracking Assembly

This is the main assembly that goes on the front of the headset. We will build it first.

Begin by soldering together the V4 Lite board. Follow the [Official Guide](https://docs.eyetrackvr.dev/how_to_build/led_setup#wiring-up-v4-lite) for this. You want to use the resistor for Dual Eye setup. In addition to the guide, also solder in 3 sets of 2x1 header pins. This will allow you to unplug stuff easier.

![Assembly 05](img/05.jpg?raw=true)

Now take off the camera hat from **one** of the ESPs and solder in 2 wires for powering the V4 Lite board. Red into VUSB, black into GND. Thread the wires from the top and solder on the bottom. Crimp together a 1x2 female dupont connector for easier unplugging. Cut off any excess solder on the bottom of the ESP so that it is flush. It should look exactly like on the image below once done. Afterwards, return the hat onto the ESP.

![Assembly 06](img/06.jpg?raw=true)

We will now do the worst part, and that is assembling the LEDs. You want to create a chain of them like shown on the images below. You can use the two `EyeRing_Bottom_L` and `EyeRing_Bottom_R` printed parts as a guideline for how long the cables should be. When soldering, always solder on the side of the PCBs where there is no LED. Don't push the wires through the holes, as the remaining solder could impede construction of the rings. **The long wire needs to be around 36cm in length.** In general, follow the image below to see exactly how to do it. Finally, crimp 1x2 dupont female connectors to the end of the long wires.

![Assembly 07](img/07.jpg?raw=true)

![Assembly 08](img/08.jpg?raw=true)

Test the assemblies to see if they work. Plug the ESP with the soldered wire into the V4 Lite board, as well as the 2 LED wires. **MIND THE POLARITY AND WHERE YOU PLUG THEM.** Polarity is marked on the V4 Lite board, or just have a look at the image below. Once plugged in, use the camera feed to verify that all of the LEDs work.

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

Place the `EyeRing_Top_L` and `EyeRing_Top_R` printed parts over the bottom ones, effectively covering the LEDs. This serves as a holding system, instead of using hotglue or some other type of glue. Secure each of the rings with 2x M2*6 Hex Head Screws and 1x M2x8 Hex Head Screw. Use the longer screw on the hole closest to the camera. Tighten the screws slowly and carefully so that the rings dont bind or break. These are small and fragile parts.

![Assembly 15](img/15.jpg?raw=true)

Place the cameras into the round half-slots and tighten them using the `EyeRing_Camera` printed parts. There is one for each eye. Use 2x M2*6 Hex Head Screws to tighten. The final eye ring assembly should look like on the image below. Do this for both left and right eyes.

This is also the point at which you can attach the heatsinks to the cameras. This is not necessary from my experience, and will significantly lower the max IPD (by around 5 mm). However, if you feel like you want to do this, you can!

![Assembly 16](img/16.jpg?raw=true)

Lay the two eyerings out on your work area and make note of how the camera cables are twisted in the image below. Make sure that they aren't tangled or anything like that. Plug in the LED wires into the V4 Lite board again. For convenience, the printed part also has small + symbols on it for wire orientation.

![Assembly 17](img/17.jpg?raw=true)

Turn the eye rings around and use electrical tape to tape the LED wires with the camera cables. You can do it every few stops in order to secure them. The result should be like on the image below. Make note of how the wires are threaded in relation to the camera cables, as well as how the camera cable is not twisted.

![Assembly 18](img/18.jpg?raw=true)

Tape the camera and LED wires up like on the image below. **Leave around 4cm of untaped cable** on the side where the extension connector is. I found that this is necessary otherwise the Index face gasket will not fit over them. On the other side, tape all the way to ESPs. Taping is important to keep the cables safe from damage. Use image below as a guide.

![Assembly 19](img/19.jpg?raw=true)

Finally, put the `Cover` printed file over the electronics and tighten it down using 3x M3*16 Hex Head Screws. Do this similar like previously with other screws.

![Assembly 20](img/20.jpg?raw=true)

The construction of the Eye Tracking Assembly is now complete! You can put it to the side while you prepare the Index itself for attaching this to it.

![Assembly 21](img/21.jpg?raw=true)

## 4. Building The Index Assembly

Begin by preparing the USB hub. Attach the USB A to USB-C adapter to it.

![Assembly 22](img/22.jpg?raw=true)

Remove the magnetic front cover on the Index and clean up the inside. Apply a double sided tape on the bottom of the frunk like on the image below.

![Assembly 23](img/23.jpg?raw=true)

Insert the `Frunk_Upper` printed part into the top of the frunk. It should latch onto the vent grills. If it doesn't you might need to adjust something with the printer's tolerances. It is a very precise fit.

![Assembly 24](img/24.jpg?raw=true)

Now plug the USB hub (via the adapter) into the USB socket on the Index.

![Assembly 25](img/25.jpg?raw=true)

Now insert the `Frunk_Lower` printed part into the frunk, while guiding the hub's cable through the slot on the side. This is a bit of a tight fit. Expect to hear creaking plastic as the printed parts' layers brush against each other. It is okay if you cannot push it all the way in, but try to do it as much as you can.

![Assembly 26](img/26.jpg?raw=true)

Prepare 2x M3*10 Counter Sunk Screws. Tighten them into the two holes on the `Frunk_Lower`. Once you are done tightening, the assembly should provide a solid base for the rest of ThoriTrack. From my experience, it cannot be removed by hand, as the upper and lower part hold themselves inside the funk. This whole assembly ensures that you don't need to disassemble your Index.

![Assembly 27](img/27.jpg?raw=true)

![Assembly 28](img/28.jpg?raw=true)

Prepare the `USB_Hub` printed part by inserting 2x M3 Nuts. They aren't held by anything so take care that they don't fall out.

![Assembly 29](img/29.jpg?raw=true)

Insert the USB hub into the printed part. Pay attention to the orientation. Nuts should be on the lower side of the Index, while USB sockets should be on the upper.

![Assembly 30](img/30.jpg?raw=true)

Tighten the `USB_Hub` printed part into the frunk assembly together with the hub itself. Use 4x M3*20 Hex Head Screws for this.

![Assembly 31](img/31.jpg?raw=true)

This might be a good moment to check if the hub assembly works. Plug in your Index into your PC and see if the hub comes online. There is a hole in the printed part which allows the white LED to be visible. You can also check if the USB-C ports work by plugging in some devices.

![Assembly 32](img/32.jpg?raw=true)

We will now prepare the face tracking arm. Take `Face_Upper` and `Face_Lower` printed parts and tighten them together using an M4 Lock Nut and an M4*20 Counter Sunk Screw. Orientation of the parts is important, so use the image below as reference. You might need to use some pliers to hold the nut in place, as it can be hard (impossible) to tighten the locking nut by hand. Tighten it enough so that the arm can be folded with acceptable resistance. You will be able to use this later to fold up your face tracking.

![Assembly 33](img/33.jpg?raw=true)

Mount both the previously built Eye Tracking Assembly and the newly built arm onto the `USB_Hub` part. Use 4x M3\*10 Hex Head Screws for the Eye Tracking and 2x M3*8 Hex Head Screws for the arm. Arm is attached to the holes where you have previously inserted the nuts. Use image below as reference.

![Assembly 34](img/34.jpg?raw=true)

We will now attach the eye rings. Remove the magnetic face gasket from the Index and pull the two loose eye ring assemblies over the top of the headset. Should be like in the image below.

![Assembly 35](img/35.jpg?raw=true)

Now carefully slide the eye rings onto the lens housings of the Index. The housings are rubber so they should neatly fit on. Take great care of the wires so you don't pinch anything. Wires should be tucked to the side of the lenses. You can also move the IPD slider a bit to see if the lenses can still move freely and that nothing is getting pinched. Check images below.

![Assembly 36](img/36.jpg?raw=true)

![Assembly 37](img/37.jpg?raw=true)

Place the face gasket back on. Take note of how the wires reach the lens area. Make sure that they are not above the screws in the frame of the Index, otherwise the magnets won't be able to snap the gasket in.

![Assembly 38](img/38.jpg?raw=true)

Use 2 of the USB-C to USB-C cables to wire up the two ESPs with the USB hub. It is okay if it pushes the camera wires off to the sides.

![Assembly 39](img/39.jpg?raw=true)

Finally, attach the Vive Facial Tracker to the bottom of the arm. Use an M4 Lock Nut and an M4*20 Counter Sunk Screw in a similar way like for the middle of the arm. Once done, plug it into the side USB port on the hub.

![Assembly 40](img/40.jpg?raw=true)

![Assembly 41](img/41.jpg?raw=true)

**And you are done! Enjoy your assembled ThoriTrack!** 

Feel free to look at the [Recommended Software](../README.md#recommended-software) section on the home page to see which software I run for best eye and face tracking.

![Assembled!](../img/Overview-Front.jpg?raw=true)