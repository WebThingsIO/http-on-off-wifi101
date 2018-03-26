Very simple HTTP server which runs on the MKR1000

By default, this server uses mDNS to advertse wifi101-XXXXXX.local
(XXXXXX will be replaced by the last 6 digits of the MAX address for the device)

Browsing to http://wifi101-XXXXXX.local/H will turn the on board LED on.

Browsing to http://wifi101-XXXXXX.local/L will turn the on board LED off.

This particular project was setup to work using PlatformIO, but it can also
be built using the Arduino IDE.

When building using PlatformIO, you may wish to edit platformio.ini and
uncomment one of these 2 lines:
```
; env_default = samw25
; env_default = mkr1000USB
```
depending on which platform you're building for.

When building using the Arduino IDE, you'll need to install the following
dependencies:

- Wifi101 - can be installed using the Library Manager
- ArduinoMDNS - needs to be installed inside the libraries directory of
  your default Arduino sketch directory. See the instructions found inside
  the http-on-off-wifi101.ino file.
