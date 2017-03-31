# Temperature/Humidity Sensor using MicroPython and Seriesly

A small project to send temperature and humidity information to the timeseries
database [Seriesly][1] for later study. Built
for NodeMCU/ESP8266 boards running MicroPython.

## Installing MicroPython

You'll need to install the correct drivers for your OS and board. For NodeMCU,
I used those found at [SiLabs][2]. You should then be able to proceed by
following the [MicroPython install instructions][3].

## Installing the code

The easiest way to do this is to connect to the board using something like
[picocom][4], enable the `webrepl`, and use the [MicroPython webrepl tool][5]
to upload the files to the board. Remember to the `settings.py` as necessary
with network and pin settings before uploading.

Once you've installed the dependencies, rebooting the board should kick things
off and you should see entries start appearing in your Seriesly server.

### Dependencies
Before the code will run, you'll need to install the dependencies below by
accessing the MicroPython REPL and running the following commands:

    >>> import upip
    >>> upip.install('micropython-logging')


[1]: https://github.com/dustin/seriesly/
[2]: https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers
[3]: https://docs.micropython.org/en/latest/esp8266/esp8266/tutorial/intro.html
[4]: https://github.com/npat-efault/picocom
[5]: http://micropython.org/webrepl/
