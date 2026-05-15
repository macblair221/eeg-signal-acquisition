# Low-Cost EEG Signal Acquisition System

A personal project building a reproducible, low-cost EEG acquisition pipeline from analog front-end hardware to eventual neural data analysis.

## Project Goal
Develop a system for collecting and analyzing EEG signals using off-the-shelf components, with the long-term aim of applying data science techniques (filtering, FFT, feature extraction, etc.) for neuroscience exploration and neurofeedback experiments.

## Current Progress

- **(Very basic) Analog Front-End Design** 
  - Simulated complete signal conditioning circuit in Tinkercad
  - Non-inverting amplifiers + active bandpass filter (≈1.6 Hz high-pass, ≈150 Hz low-pass)
  - 2.5V DC biasing for Arduino Nano ADC compatibility
  - Total gain ≈ 22

- **Hardware**
  - Hand-drawn schematics completed
  - Components sourced
  - Basic Arduino Nano Every testing and breadboard prototyping done

- **Software**
  - Basic Arduino firmware tested (serial communication)

## Gallery

<img src="images/Analog_FrontEnd_TinkerCAD_Schematic.jpg" width="420" alt="Hand-drawn EEG Analog Front-End Schematic">
<img src="images/LTspice_OpAmp_Bandpass.jpg" width="420" alt="LTspice Schematic of Analog Front-End">

## Next Steps

- Build and test physical circuit with electrodes
- Implement real-time data collection with Arduino
- Develop Python pipeline (serial reading, filtering, FFT, visualization)
- Explore basic signal processing techniques

## Tech Stack
- **Hardware**: Arduino Nano Every, AD620 Instrumentation Amp, 2x TL084CN OpAmps, Trimpot, Gold Plated Electrodes
- **Simulation/Design**: Tinkercad, LTspice
- **Planned**: Python, NumPy, SciPy, Matplotlib

