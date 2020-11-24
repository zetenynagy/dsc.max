# DSC_Max
Preconfigured Max/MSP abstractions for using Sony DualSense and DualShock 4 controllers as input devices in the Max environment via HID.

**Features:**
* Support for DualSense (dsc.ds5) and DualShock 4 (dsc.ds4)
* Analog stick absolute position detection
* L1, L2, L3, R1, R2, R3 button press detection
* L2/R2 trigger pressure detection
* 8-way D-Pad direction detection
* Action buttons press detection
* Create/Share button and Options button press detection
* PS button, Mute button (DualSense) and touchpad click detection
* Touchpad Y-axis detection with 2-finger multitouch
* DualSense built-in microphone support
* DualSense haptic feedback support - see Examples.maxpat
* Roll and Pitch detection using gyroscope
* Simple, easy-to-use annotated outputs
* Easily editable and expandable in Max

**How to use?**
* To use, simply connect your controller via USB, then open Max and create a new patcher. After adding your controller's designated dsc_max object (dsc.ds5 for DualSense, dsc.ds4 for DualShock 4), connect the first outlet of dsc_max to the inlet of an umenu object. Then connect the second (middle) outlet of the aforementioned umenu to the second (middle) inlet of dsc_max. Send a bang on the first inlet of dsc_max, then select the device in the umenu. Connect the outlets to your liking, then toggle polling on the third (right) inlet. (See Example.maxpat)

**Dependencies and requirements:**
* Max/MSP is required to use this patcher.
* A Sony DualSense or DualShock 4 controller and their respective compatible USB cables are required.

**Planned features:**
* Touchpad X-axis detection and output
* Full gyroscope and accelerometer detection and output
* Two-way communication to enable light bar, rumble, built-in speaker and Adaptive Trigger (DualSense) motor control
* Battery level reading
* DualSense microphone input gain support
* Wireless support via Bluetooth
* Full compatibility with DualShock 3
* Full transition to [hidapi](https://github.com/NullMember/maxhidapi) insted of Max's built-in [hi] object, for hotswapping and easy two-way communication

**Known bugs:**
* Max will not detect the controller if it was already open when it was plugged in. Please completely shut down Max, connect the controller via USB, then open it up again. This seems to be a limitation of the built-in [hi] object.

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
