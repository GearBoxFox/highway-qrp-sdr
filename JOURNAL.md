# Project Name Here

I got my amateur radio license late last year, and have been itching to use it more since then. I've decided this summer to work more on using it, but to that extent I need a radio. CW (morse code) seems pretty interesting, and working on the long range HF bands seems like a fun challenge, so I decided to build a 5w CW Software Defined Radio based off the RP2350 chip.

## May 14

Highway kicked off today, and with it come many new projects.
I've never built any kind of RF device before, so this is entirely new territory for me.
I decided to do some research into the general design of a transceiver.
The first thing that I've found is a series of schematics from [QRP-Labs](https://qrp-labs.com/) that details their QCX-mini transceiver. I then found a series by HAM operator Ward Harriman, AE6TY, [detailing the design of a QRP SDR](https://www.ae6ty.com/wp-content/uploads/2024/06/QRP-SDR-1a.pdf) which I have a feeling I'll be utilizing frequently.

![AE6TY's SDR block diagram](./assets/ae6ty_block_diagram.png)

In his guide, he details a block diagram which I'm going to reference for my own board. The design I intend to use will have four main parts:

1. The MCU, which will handle all the digital signal processing, IO to a display, key, etc.
2. A "Tayloe" Detector, which will convert the RF received from the antenna into an I and Q analog input on the RP2350
3. Filters, of some sort, on the transmit and receive (IDK I'm not an RF engineer).
4. An amplifier on the transmit end, to bump the power up to 5W.

There will probably be other features, like a Li-Ion battery charger, but my final idea is somewhere inbetween the [QRP QCX-mini](https://qrp-labs.com/qcxmini.html) and the [HF Signals zBitx](https://www.hfsignals.com/index.php/zbitx/).
