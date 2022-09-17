# RPi-Pico-W
PlatformIO/Arduino C/C++ Examples For The Raspberry-Pi Pico-W

**NOTE** The example code presented in this directory is entirely based on the work of others and, although I have uploaded my version under the Apache-2 license, it may also be covered by different licenses from any of the original authors, including, but not limited to:-
- Michael Margolis
- Paul Stoffregen
- Earl F.Philhower III
- Maximilian Gerhardt


## Use
I'm assuming that, by virtue of being here, you already have PlatformIO installed.  In that case you really just need to do "pio run" and the settings in the platformio.ini will cause the support framework for the Pico-W to be automatically downloaded.

Once the firmware is built, you'll find the firmware.uf2 file in:-  .pio/build/rpipicow/

The simplest way to upload it to the Pico-W is to hold the button down on the Pico-W board while plugging it into a USB port and then just copy the firmware.uf2 file to /media/XXXXX/RPI-RP2 (where "XXXXX" is your username). If you're that way inclined, you can drag-and-drop the file there, instead.

Once the file is uploaded, the Pico will automatically unmount the /media/XXXXX/RPI-RP2 filesystem and restart.  Your system should then automatically create /dev/ttyACM0, allowing you connect using minicom, screen or whatever terminal-emulation program you prefer (the baud rate is 115200).

The initial start-up messages will tell you what IP address the Pico-W has been assigned on your network (you should be able to ping it at this point) and the host name of the NTP server to which it is trying to connect.  From that point (assuming the NTP call succeeded) you should see the date and time incrementing every second.  The on-board LED on the Pico-W should be toggling on and off as the seconds change, too.



