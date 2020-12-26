# dsc.max
Preconfigured Max/MSP abstractions for using various game controllers as input devices in the Max environment via HID.

**Features:**
* Supported controllers:
  * Sony DualSense (*dsc.ds5.usb* via USB and *dsc.ds5.bt* via Bluetooth)
  * Sony DualShock 4 (*dsc.ds4.usb* via USB)
  * Xbox One Controller (*dsc.xbo.bt* via Bluetooth)
* Analog stick absolute position detection
* L1, L2, L3, R1, R2, R3 (LT, LB, LS, RT, LB, RS) button press detection
* L2/R2 (LT/RT) trigger pressure detection
* 8-way D-Pad direction detection
* Action buttons press detection
* Create/Share button and Options button press detection
* PS button, Mute button (DualSense, USB only) and touchpad click detection
* Touchpad Y-axis detection with 2-finger multitouch (DualShock 4 and DualSense, USB only)
* DualSense built-in microphone support (USB only)
* DualSense haptic feedback support (USB only) - see Example.maxpat
* Roll and Pitch detection using gyroscope (DualShock 4 and DualSense, USB only)
* Simple, easy-to-use annotated outputs
* Easily editable and expandable in Max

**How to use?**
* To use, simply connect your controller via USB or BT, then open Max and create a new patcher. After adding your controller's designated dsc.max object (dsc.ds5 for DualSense, dsc.ds4 for DualShock 4, dsc.xbo for Xbox One controller, .bt or .usb suffixes for their respective connections), connect the first outlet of dsc.max to the inlet of an umenu object. Then connect the second (middle) outlet of the aforementioned umenu to the second (middle) inlet of dsc.max. Send a bang on the first inlet of dsc.max, then select the device in the umenu. Connect the outlets to your liking, then toggle polling on the third (right) inlet. (See Example.maxpat)

**Dependencies and requirements:**
* Max/MSP is required to use this patcher.
* A supported controller, cable and USB port, Bluetooth capabilities.

**Upcoming features - currently work in progress, slated for the next update:**
* Full USB compatibility with Google Stadia Controller (*dsc.sta.usb* abstraction)

**Planned features:**
* Touchpad X-axis detection and output (DualShock 4 and DualSense only)
* Full gyroscope and accelerometer detection and output (DualShock 4 and DualSense only)
* Two-way communication to enable audio jack support, Xbox button (Xbox One controller only), light bar (DualShock 4 and DualSense), rumble, built-in speaker (DualShock 4 and DualSense), Mute Button Light (DualSense Only) Adaptive Triggers (DualSense only), Haptic Triggers (Xbox One controller only)
* Battery level reading
* DualSense microphone input gain support
* DualShock 4 wireless support via Bluetooth
* DualSense full feature support via Bluetooth
* Xbox One controller USB support
* Full USB and BT compatibility with Sony DualShock 3
* Full USB and BT compatibility with Xbox Elite Controller 2
* Full USB and BT compatibility with Xbox Series Controller
* Full USB and proprietary wireless compatibility (via adapter) with first generation Xbox One controller and first generation Xbox Elite controller
* Full compatibility with Xbox Adaptive Controller
* Possible integration with PlayStation Move controller
* Full BT compatibility with Nintendo Wii Remote
* Full USB and BT compatibility with Nintendo Switch Joy-Cons
* Full USB and BT compatibility with Nintendo Switch Pro Controller
* Possible integration with various VR controllers
* DualShock 4 official Sony back button extension support
* Full transition to [hidapi](https://github.com/NullMember/maxhidapi) insted of Max's built-in [hi] object, for hotswapping and easy two-way communication

**Known bugs:**
* Max will not detect the controller if it was already open when it was plugged in. Please completely shut down Max, connect the controller via USB first, then open it up again. This seems to be a limitation of the built-in [hi] object.
* Might not work on Windows, working on testing via Boot Camp
* Bluetooth gamepad connections might not be supported on macOS versions older than 10.15 Catalina.

**Tested and working on:**
* Max/MSP 8.1.5, macOS Catalina 10.15.7
  
"PlayStation", "PlayStation Family Mark", "PS5 logo", "PS5", "DualSense" and "DUALSHOCK" are registered trademarks or trademarks of Sony Interactive Entertainment Inc. "SONY" is a registered trademark of Sony Corporation.
This software is NOT affiliated with Sony, and does NOT mean to infringe it's copyrights and trademarks. This software was created under Fair Use.

Max/MSP Copyright (c) 2015, Cycling '74.
All rights reserved.

The developer of this software is not responsible for and can not be held liable for any damages done to an end user's equipment. Use at your own risk. THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Sources:
[DS4Windows DualSense support ticket thread](https://github.com/Ryochan7/DS4Windows/issues/1545)
[Reddit post by u/ginkgobitter](https://www.reddit.com/r/gamedev/comments/jumvi5/dualsense_haptics_leds_and_more_hid_output_report/?sort=new),
[Reddit post by u/Demonchaser27](https://www.reddit.com/r/PS5/comments/jnp8tu/heres_how_to_get_audio_haptic_feedback_with/)
