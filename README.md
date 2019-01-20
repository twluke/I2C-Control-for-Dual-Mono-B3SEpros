# I2C-Control-for-Dual-Mono-B3SEpros

This is a set of I2C config files: for right and left channels, respectively.

Requirement: a pair of B3SEpros with firmware removed, a BBB with a botic-debian system connected to Hermes-BBB and Cronus.

Before using this set, you have to connect the I2C cables (4 lines: 3.3V, SCL, SDA and GND) from the isolated I2C header of the Hermes-BBB to each DAC, respectively.

The DAC_RESET and DVCC must be shorted by a jumper with an extra wire from it to connect the reset pin of each DAC.

Short the DAC_ADDR(11) and DVCC(12) of the second DAC to set a different address (0x49).

The analog output from the main DAC (address 0x48) is used for the left channel and the other from the second DAC (address 0x49) for the right channel.

Then power on and confirmm that you get the right sound.
