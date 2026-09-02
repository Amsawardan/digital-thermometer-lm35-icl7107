# Digital Thermometer using LM35 and ICL7107

## Overview

This project was developed as the final assignment for the **IE2044 – System Modeling and Prototyping** module.

The project focuses on the design and implementation of a **2-digit digital thermometer capable of measuring temperatures from 0°C to 99°C**.

The system uses an **LM35 temperature sensor** to generate an analog voltage proportional to temperature. An **ICL7107 dual-slope ADC and display driver** converts the analog signal into a digital value and directly drives two 7-segment displays.

The project was developed through three main stages:

1. Circuit design and analysis
2. Proteus simulation
3. EasyEDA PCB design and physical implementation

## Features

* Temperature measurement from **0°C to 99°C**
* LM35 analog temperature sensor
* ICL7107 ADC and 7-segment display driver
* Dual 7-segment digital display
* 100 mV reference voltage for calibration
* Proteus circuit simulation
* EasyEDA PCB design
* Physical PCB implementation and testing
* Calibration using a potentiometer

## Components

| Component         | Quantity | Purpose                         |
| ----------------- | -------: | ------------------------------- |
| LM35              |        1 | Temperature sensing             |
| ICL7107           |        1 | ADC and display driver          |
| 7-Segment Display |        2 | Temperature display             |
| Potentiometer     |        1 | Reference voltage adjustment    |
| Resistors         | Multiple | Circuit operation and filtering |
| Capacitors        | Multiple | Filtering and stability         |

## Working Principle

The LM35 produces an output voltage proportional to temperature at approximately **10 mV/°C**.

For example:

* 25°C → 250 mV
* 50°C → 500 mV
* 99°C → 990 mV

The ICL7107 converts the sensor voltage into a digital value and drives the two 7-segment displays.

A reference voltage of approximately **100 mV** is used for calibration so that the displayed value corresponds to the measured temperature.

## Proteus Simulation

The complete circuit was simulated using Proteus.

The simulation includes:

* LM35 temperature sensor
* ICL7107 ADC/display driver
* Two 7-segment displays
* Reference voltage adjustment
* Supporting resistors and capacitors

### Simulation Results

| Temperature | Sensor Voltage | Display |
| ----------: | -------------: | ------: |
|         0°C |            0 V |      00 |
|        25°C |         250 mV |      25 |
|        50°C |         500 mV |      50 |
|        99°C |         990 mV |      99 |

The simulation demonstrated the expected relationship between temperature, sensor voltage and displayed value.

## PCB Design

The circuit was converted into a PCB using **EasyEDA Pro**.

During PCB design, attention was given to:

* Component placement
* Short analog signal paths
* Clean routing
* 7-segment display alignment
* Temperature sensor placement

The LM35 sensor was positioned so that it could be placed outside the main PCB area for practical temperature measurement.

## Hardware Implementation

After completing the PCB design, the circuit was assembled and tested as a physical prototype.

The display responded to temperature changes and the reference voltage was adjusted using the calibration potentiometer.

During testing, minor fluctuations were observed and reduced through grounding improvements.

## Results

The project successfully demonstrated a functional digital thermometer for the **0°C–99°C** measurement range.

The main practical observations included:

* Correct temperature display
* Successful LM35 sensor operation
* Successful ICL7107 ADC operation
* Successful PCB implementation
* Calibration using the reference voltage
* Sensitivity to small analog voltage variations

## Challenges

One of the main challenges was the sensitivity of the LM35 output because the sensor produces only **10 mV per °C**.

Small power-supply variations and external noise could therefore affect the least significant digit.

The project also highlighted the importance of:

* Proper grounding
* Stable power supplies
* Accurate reference-voltage calibration
* Careful PCB routing
* Separation of analog and digital signal paths

## Repository Structure

```text
digital-thermometer-lm35-icl7107/
│
├── documentation/
├── simulation/
├── pcb/
├── hardware/
└── README.md
```

## Team Members

**Group 11**

* IT24101644 – N.K.B.A.G.A.I. Narasinghe
* IT24103484 – B. Amsawardan

## Documentation

The complete project report is available in:

`documentation/IE2044-Digital-Thermometer-Report.pdf`

## References

* Texas Instruments – LM35 Datasheet
* Renesas – ICL7107 Datasheet
* IE2044 Lecture Notes
* Proteus Documentation
* EasyEDA Documentation
