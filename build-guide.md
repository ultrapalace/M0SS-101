M0SS-101 BUILD GUIDE \- updated Sept 14, 2025

Here are the contents of the kit

![image 1](/images/image1.jpg)

**STEP 1: Remove the edge rails from all PCBs**

- Using pliers, carefully snap off the edge rails. There are rails on the left and right sides of each PCB, 6 edges in total to be removed.

![][image2]

**STEP 2: Place and solder the encoder**

- Confirm you are placing the encoder on the correct side, by checking for the white outlined shape of the part, drawn on the PCB. The encoder goes on the back side.  
- Slightly bend the lugs of the encoder inward, using pliers, or by gently pressing them into the table.  
- Carefully place the encoder. If the lugs will not go in, bend them inward a little more.  
- Solder one pin of the encoder, and check that it is seated correctly.  
- Proceed to solder all the pins, and then the lugs.

![][image3]

**STEP 3: Place and solder the DC jack, audio jack and USB jack**

- These parts are placed on the top side of the main PCB, look for the footprint outlines to confirm, these are installed on the opposite side as the encoder.  
- Start with the DC jack, and solder one pin, then adjust the position of the jack to be as square and straight as possible, using the white footprint outline, before soldering the remaining 2 pins.  
- Now place, and then solder, the USB jack and the audio jack.

![][image4]

**STEP 4: Install the standoff**

- The standoff goes on the same side as the encoder, the back side of the main PCB.  
- Use a small screw, and be careful to not over tighten it. ⅛ of a turn past hand-tight is great.

![][image5]

**STEP 5: Install the Flat Flex Cables (FFCs).**

- Install the large FFC onto the back side of the front panel board. The large FFC connector is a flip-lock type. Using a small tool or a fingernail, lift the black lock up and back to fully open the connector.   
- Insert the large FFC with the blue stripe up. Ensure it is fully seated and square, then close the lock.

![][image6]

- Install the small FFC onto the LED board. The small FFC connector is a drawer-type. Using a small tool or a fingernail, gently pull laterally on the black lock to open it like a drawer.  
- Insert the small FFC with the blue stripe up, sliding it under the lock, and gently wiggle it into place. This may take some patience, and it is ok to try the other end, if you are struggling.  
- Lock the connector by pressing the drawer back into the closed position.

![][image7]

**STEP 6: Assemble the stack-up.**

- Thread the large FFC through the large cutout in the LED board, and bring the 2 boards together back-to-back.

![][image8]

- Holding the main board with the encoder facing down toward the other boards, thread the small FFC through the smaller slit in the main board, and thread the large FFC through the wide slit in the main board. Pass the encoder through the large round hole in the 2 other boards

![][image9]  
![][image10]  
![][image11]

- On the front panel board, install the encoder nut, and the small screw to the standoff. When tightening the encoder nut, exercise caution to not scratch the panel, and to not damage any adjacent buttons. Using a plastic socket is ideal.

![][image12]

**STEP 7: Connect the FCCs to the main board.**

- Use the same procedure in step 5 to install both FFCs to their respective connectors on the main board.


![][image13]  
![][image14]

**STEP 8: Program the microcontroller**

- Download the binary file m0ss-101.bin  
- Download Bouffalo Labs Dev Cube.  
- Open Bouffalo Labs Dev Cube (it may take a while to open)  
- Select “BL616/618” from the initial prompt.  
- Click the “MCU” tab.  
- Leave all the settings at their defaults.  
- Click “Browse” to select an Image File (ignore Device Tree), and select the binary file m0ss-101.bin from your computer.

![][image15]

- Using a USB Type-B cable, connect your computer to the M0SS-101 using the small usb connector on the side of the main board (not the large USB-A connector on the back side).  
- Using a 9v DC, center-negative PSU, apply power to the M0SS-101 via the DC Jack.

![][image16]

- Press the small button on the main board of M0SS-101 labelled “rst” while holding the other button labeled “boot”.  
- In Bouffalo Labs Dev Cube click “Refresh”.  
- A new serial port should appear in Bouffalo Labs Dev Cube, in the field labeled Port/SN.  
    
  ![][image17]  
    
- Click “Create and Download”. The progress bar should move to 100% and turn green for success.  
- Reset the microcontroller on M0SS-101 by pressing the small button on the main board labelled “rst”.  
- Confirm that some LEDs are now glowing, which indicates that the flash was successful.

**STEP 9: Install the enclosure**

- Disconnect the USB cable and the 9v DC PSU.  
- Place the PCB assembly into the enclosure, inserting the jacks first.  
- Install the 4 large black screws.  
- Install the plastic washer and nut onto the audio jack.  
- Install the knob onto the encoder, looking for the irregularity inside the knob, which mates with the flat side of the encoder shaft.  
- Optionally, affix the 4 adhesive feet, on the bottom of the enclosure, at each corner.

![][image18]  
![][image19]  
![][image20]

**STEP 10: Test your M0SS-101**

- While holding the “ALT” and “VOL” buttons, apply power to the M0SS-101.  
- Confirm that all the LEDs are glowing yellow.  
- Press each button, and confirm that the LEDs turn red.  
- Connect the audio jack to an amplifier or a scope, and confirm that a 110hz (A2) square wave is present.  
- Connect a MIDI device to the USB-A jack, send some MIDI, and confirm that the LEDs flash blue.  
- Connect a MIDI device to the ⅛” MIDI input jack (the one closer to the back), send some MIDI, and confirm that the LEDs flash blue.  
- Turn the encoder clockwise, and confirm that the LEDs flash green.  
- Turn the encoder counter-clockwise, and confirm that the LEDs flash blue.
