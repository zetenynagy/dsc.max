# DSC_Max
A Max/MSP patcher for using Sony DualSense controllers as input devices in the Max environment via HID.
Version 0.1 - Initial alpha release

**Features:**
* Analog stick absolute position detection
* L1, L2, L3, R1, R2, R3 button press detection
* L2/R2 trigger pressure detection
* 8-way D-Pad direction detection
* Action buttons press detection
* Create button and Options button press detection
* PS button, Mute button and touchpad click detection
* Touchpad Y-axis detection with 2-finger multitouch
* Simple, easy-to-use annotated outputs
* Easily editable and expandable in Max

**How to use?**
* To use, simply connect your controller via USB, then open Max and create a new patcher. After adding the dsc_max object, connect the first outlet of dsc_max to the inlet of an umenu object. Then connect the second (middle) outlet of the aforementioned umenu to the second (middle) inlet of dsc_max. Send a bang on the first inlet of dsc_max, then select the device in the umenu. Connect the outlets to your liking, then toggle polling on the third (right) inlet. (See Example.maxpat)

**Dependencies and requirements**
* Max/MSP is required to use this patcher.
* Because of the fast (10ms) polling speed, a dual-core Intel Core 2 Duo or better is recommended.

**Planned features:**
* Touchpad X-axis detection and output
* Full gyroscope and accelerometer detection and output
* Built-in microphone sound detection
* Two-way communication to enable light bar, haptic feedback, rumble, built-in speaker and Adaptive Trigger motor control
* Wireless support

**Known bugs:**
* Max may not detect the controller if it was already open when it was plugged in. Please completely shut down Max, connect the controller via USB, then open it up again.
* Tested and working on:
  * Max/MSP 8.1.5, macOS Catalina 10.15.7
  
"PlayStation", "PlayStation Family Mark", "PS5 logo", "PS5", "DualSense" and "DUALSHOCK" are registered trademarks or trademarks of Sony Interactive Entertainment Inc. "SONY" is a registered trademark of Sony Corporation.
This software is NOT affiliated with Sony, and does NOT mean to infringe it's copyrights and trademarks. This software was created under Fair Use.
