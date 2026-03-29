# novadac
6-ch, 12-bits DAC + 2-ch. 16-bits parallel out for Nova. Compatible with 4037.

Device code 23. Use DOB to select channel (0-5 for DACs, 6-7 for parallel out). Use DOA for data.
There is also oscilloscope blanking (Z control), untested, following the 4037 description.

The board includes op-amps on DAC outputs for protecting the DACs. With the given R-C values there is a ca. 10 kHz cut-off for noise reduction.

Note two problems with the PCB:
* Produced with 1.6 mm thickness is very difficult to insert into slot (but you can do it!)
* The DAC output connectors are made for vertical minijacks. This is stupid because it requires at least 3 slots. You probably want to solder in something else there. The parallel-out screw connectors are also too tall for 1 slot. (I have plenty of space in my Nova 840)

Have not made bill-of-materials. Components are in the schematic, the chips are:
U1, U2, U3, U5: 74LS04
U4: 74LS30
U6: 74LS08
U7: 74LS75
U8: 74LS138
U9, U10, U11, U12: 74LS374 (only needed for parallel out)
U13, U14, U15: AD7247 dual 12-bits DA converters (only U13 needed for 2-channel)
U16, U17, U18: LM6142 (only U16 needed for 2-channel)
U19, U20: 74LS122 (Z-control)

The AD7247 is expensive and difficult to get. Bad choice of chip, sorry.
