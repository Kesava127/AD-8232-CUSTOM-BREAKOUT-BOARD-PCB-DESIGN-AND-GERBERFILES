 AD8232 Breakout Board

A custom ECG signal acquisition breakout built around the AD8232 analog front-end IC.
This board is designed to amplify and filter weak biopotential signals from the human body, making them suitable for reading by microcontrollers such as ESP32, Arduino, or other data logging systems.

 Features

Core IC: AD8232 – Low-power, single-lead ECG front-end

Input Connector (J2): 3.5 mm jack for ECG electrodes

Output Connector (J3): 6-pin header for MCU interface (OUTPUT, LO+, LO–, 3.3 V, GND, etc.)

Power Connector (J1): JST input, 3.3 V supply

Filter Network: Configurable high-pass and low-pass filters for clean ECG waveform extraction

Compact Layout: Small and wearable-friendly design

Clear Silkscreen Labels: Simplifies assembly and debugging

 Applications

ECG and heartbeat monitoring

Biomedical instrumentation

Wearable health systems

Signal processing and biosensor R&D

Educational or prototyping projects

 Design Details

Software: Altium Designer

Layers: 2-layer PCB

Board Size: Compact form factor for easy integration

Designer: KESAVA

 Usage
 Hardware Setup

Connect Electrodes
Plug your ECG electrode cable into the 3.5 mm jack (J2).

RA → Right arm

LA → Left arm

RL → Right leg (ground/reference)

Connect to Microcontroller (J3 pins)

Pin	Description
3.3V	Power supply (3.0–3.3 V only)
GND	Ground
OUTPUT	Analog ECG output
LO+	Lead-off detection +
LO–	Lead-off detection –
