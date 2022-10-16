# Interface

Modified SPI with a flow control bit. Unlike PS1, there are 4 dedicated SPI lanes. Bus runs at up to 24 Mhz, however some commands are sent at lower frequencies. For example, the MagicGate handshake during boot is done at 8 Mhz, and a game was observed to send the select read sector at 4 Mhz (while the following data read is 24 Mhz).

## Termination

On the card side, measured from an official memory card SCPH-10020:

* DAT: 22ohm
* CMD: 300ohm
* SEL: 22ohm
* CLK: 300ohm
* ACK: 22ohm
