# Low-Cost EEG Signal Acquisition System

A personal project building a reproducible, low-cost EEG acquisition pipeline from analog front-end hardware to eventual neural data analysis.

## Project Goal

Develop a low-cost system for collecting and analyzing EEG-style biosignals using off-the-shelf components. The long-term goal is to combine analog signal conditioning, Arduino-based data capture, and Python-based signal processing for exploratory neuroscience and neurofeedback experiments.

This project is for learning, prototyping, and non-medical experimentation only.


## Current Progress

### Analog Front-End Design 
- Created an early analog front-end prototype in Tinkercad to model signal conditioning, amplification, filtering, and Arduino-compatible 2.5V biasing
- Rebuilt the core front-end architecture in LTspice for more rigorous circuit simulation
- Designed and simulated a signal chain consisting of:
  - RC high-pass filtering for low-frequency drift reduction
  - Two non-inverting op-amp gain stages
  - RC low-pass filtering for high-frequency attenuation
  - AC coupling into a 2.5V Arduino-compatible bias node
- Verified circuit behavior using:
  - AC analysis to inspect frequency response and gain
  - Transient analysis to test sine-wave inputs at different frequencies
- Current LTspice version uses an approximate passband of ~0.5 Hz to ~40 Hz with total simulated gain of approximately 121x

### Hardware 
- Completed hand-drawn schematic planning
- Sourced major components for breadboard-level testing
- Tested basic Arduino Nano Every setup and simple breadboard circuits
- Planning physical signal-chain testing before connecting electrodes

### Software
- Tested basic Arduino serial communication
- Planned Python pipeline for:
  - Serial data reading
  - Signal visualization
  - Digital filtering
  - FFT analysis
  - Feature extraction

## Gallery

<img src="images/Analog_FrontEnd_TinkerCAD_Schematic.jpg" width="420" alt="Hand-drawn EEG Analog Front-End Schematic">
<img src="images/LTspice_OpAmp_BandPass.jpg" width="600" alt="LTspice Schematic of Analog Front-End">

## Repository Structure

```text
ltspice/
  eeg_frontend_v1_ac_analysis.asc
  eeg_frontend_v1_transient.asc

images/
  Analog_FrontEnd_TinkerCAD_Schematic.jpg
  LTspice_OpAmp_BandPass.jpg
  ...
  ...
```

## Next Steps

- Continue LTspice refinement using more realistic op-amp models
- Build and test the physical circuit in isolated, battery-powered conditions
- Validate amplifier and filter stages with known test signals before using electrodes
- Implement Arduino-based real-time data collection
- Develop Python analysis tools for visualization, filtering, FFT, and feature extraction
- Document results and limitations as the project develops

## Tech Stack
- Hardware: Arduino Nano Every, AD620 instrumentation amplifier, TL084CN op-amps, resistors, capacitors, trimpot, electrodes, Zener diodes
- Simulation/Design: Tinkercad, LTspice
- Planned Analysis: Python, NumPy, SciPy, Matplotlib

