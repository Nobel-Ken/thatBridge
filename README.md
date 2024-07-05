# thatBridge - An Analog to Digital Bridge Device
## About
The "thatBridge" is an analog-to-digital converter board that allows for readings from "The Analog Thing" Analog Computer to be digitized and analyzed. It's based on an RP2040 microcontroller and its firmware was written with its C SDK. It can do both intermittent sampling (for a live oscilloscope view) and continuous sampling and streaming to a PC. It can record 4 channels at up to 500 kilo-samples a second with a sample depth of 8 bits. Samples are sent over USB and the device shows up as a USB CDC serial device on the host PC. The device also triggers the correct signals for the "The Analog Thing" to sweep its output in coordination with sample recording.

A host client is also provided to run on the PC and act as an interface for data collection. It allows parameters for recording to be selected and also for data to be viewed and saved. The host client is written in Python with the UI provided using QT5.

![thatBridge](https://github.com/Nobel-Ken/thatBridge/assets/17792367/f742fe14-470d-43bb-924e-ff7359f5dcb1)

## How to Use

