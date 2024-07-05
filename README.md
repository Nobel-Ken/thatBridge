# thatBridge - An Analog to Digital Bridge Device
## About
The "thatBridge" is an analog-to-digital converter board that allows for readings from "The Analog Thing" Analog Computer to be digitized and analyzed. It's based on an RP2040 microcontroller and its firmware was written with its C SDK. It can do both intermittent sampling (for a live oscilloscope view) and continuous sampling and streaming to a PC. It can record 4 channels at up to 500 kilo-samples a second with a sample depth of 8 bits. Samples are sent over USB and the device shows up as a USB CDC serial device on the host PC. The device also triggers the correct signals for the "The Analog Thing" to sweep its output in coordination with sample recording. Sample acquisition is done via DMA and is synced with the ADC so that samples aren't repeated or skipped.

A host client is also provided to run on the PC and act as an interface for data collection. It allows parameters for recording to be selected and also for data to be viewed and saved. The host client is written in Python with the UI provided using QT5.

The PCB is a simple two-layer board that breaks out the correct signals into the 16-pin block connector that matches the one found on "The Analog Thing". It was designed in KiCad and manufactured by JLCPCB.

![thatBridge](https://github.com/Nobel-Ken/thatBridge/assets/17792367/f742fe14-470d-43bb-924e-ff7359f5dcb1)

## How to Use

1. Solder a WaveShare RP2040 Zero board to the PCB, along with a 16-pin block connector.
2. Flash the UF2 onto the RP2040 Zero by holding the boot button, plugging the thatBridge into a PC, and then dragging the appropriate UF2 file onboard.
3. Run the Python client and connect to the device.



