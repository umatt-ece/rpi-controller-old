# rpi-controller-old

This is all the code I could find on the Raspberry Pi in the shop. From what I've been told, it should be functional,
it was used in previous years. However, there is no documentation and is fairly messy. I do not know the original
author. Apparently, the C-code written for the PCB design in 2020 was based off this code, so that might be another
valuable source of information while parsing through these files.

## Notes about the Code

- The important python files are in [P22](./Documents/P22). Largely these files control the setup/updating of the GUI.
- The logic and GPIO interfacing is mostly in [Drive.py](./Documents/P22/Drive.py).
- The existing code uses the python module RPi.GPIO and then seems to do a bunch or obscere stuff to implement Serial
Peripheral Interface (SPI). I think we should look into other libraries (ex.
[gpiozero](https://gpiozero.readthedocs.io/en/stable/) or [pigpio](https://abyz.me.uk/rpi/pigpio/python.html)) which
already have this implemented.
