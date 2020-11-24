# DSC_Max
# Experimental branch - hidapi transition
**This is an experimental build. Please use main branch or release version.**

*A version of DSC_Max that is based on [maxhidapi](https://github.com/NullMember/maxhidapi) and by extension [hidapi](https://github.com/libusb/hidapi) instead of Max's built-in [hi] object.*

Whether it is the main branch, or an experimental one, use DSC_Max at your own risk.

**Pros**
* Ability to hotswap controllers, can connect and disconnect at any time via USB without locking up Max
* Easier data routing
* Possible bluetooth connection
* Possible two-way communication: enables use of rumble, adaptive triggers, light bar etc.
* Way less convoluted to set up: just needs a toggle to run
* Lower level: theoretically consumes less CPU power

**Cons**
* Button data comes out in a very different way, still no solution for it, would be very hard and inefficient to route them
* DualShock 4 touchpad click and PS button data are nowhere to be found somehow

**Known issues**
* Currently very CPU intensive for some reason, this also introduces some latency
* Bluetooth connections result in an error

*This branch will eventually replace the old, [hi] based one. That will happen when all major bugs are ironed out, and feature parity is achieved.*
  
"PlayStation", "PlayStation Family Mark", "PS5 logo", "PS5", "DualSense" and "DUALSHOCK" are registered trademarks or trademarks of Sony Interactive Entertainment Inc. "SONY" is a registered trademark of Sony Corporation.
This software is NOT affiliated with Sony, and does NOT mean to infringe it's copyrights and trademarks. This software was created under Fair Use.

Max/MSP Copyright (c) 2015, Cycling '74.
All rights reserved.

The developer of this software is not responsible for and can not be held liable for any damages done to an end user's equipment. Use at your own risk. THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Special thanks to GitHub user [NullMember](https://github.com/NullMember) and everyone behind [hidapi](https://github.com/libusb/hidapi) for making amazing software for everyone.

Sources:
[DS4Windows DualSense support ticket thread](https://github.com/Ryochan7/DS4Windows/issues/1545)
[Reddit post by u/ginkgobitter](https://www.reddit.com/r/gamedev/comments/jumvi5/dualsense_haptics_leds_and_more_hid_output_report/?sort=new),
[Reddit post by u/Demonchaser27](https://www.reddit.com/r/PS5/comments/jnp8tu/heres_how_to_get_audio_haptic_feedback_with/)
