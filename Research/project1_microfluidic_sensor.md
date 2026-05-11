[project1_microfluidic_sensor.md](https://github.com/user-attachments/files/27613502/project1_microfluidic_sensor.md)
# Project 1: Soft Polymer Microfluidic Tactile Sensor

## Overview

Designed and fabricated end-to-end soft polymer (PDMS) microfluidic tactile sensors for noninvasive arterial pulse signal acquisition at the radial and carotid arteries.

---

## Motivation

Existing wearable cardiovascular sensors — particularly PPG-based optical sensors — suffer from well-documented performance limitations related to skin pigmentation, ambient light, and motion artifacts. A mechanical tactile sensor that measures arterial wall displacement directly offers a sensing modality that is independent of these optical limitations and can provide richer biomechanical information about arterial stiffness.

---

## What I Did

### Fabrication Process
- **CAD design** of electrode patterns and microchannels using AutoCAD
- **Photolithography**: spin coating, UV exposure, development of Au/Cr electrode patterns (100 nm/10 nm) on Pyrex slides
- **Sputter deposition** (EMS300T D) and lift-off for thin-film electrode patterning
- **SU-8 microchannel mold fabrication** (100–150 μm channel height)
- **PDMS casting** at 10:1 elastomer-to-curing-agent ratio (Sylgard 184)
- **Plasma bonding** of PDMS-to-Pyrex (PDC-001 oxygen plasma treatment)
- **Electrolyte filling** via syringe through reservoir holes
- **3D-printed molds** explored as a time-effective alternative to SU-8-based molds

### Readout Electronics
- Designed **5-channel custom PCBs** (KiCad) for analog readout
- Circuit: **Transimpedance amplifier** (OPA656U) + **AD835-based demodulation** (multiplier + 3rd-order 100 Hz LPF)
- Five parallel channels for simultaneous multi-transducer readout
- NI DAQ digitization with real-time **LabVIEW** monitoring

### Sensor Characterization
- Characterized static performance using micropositioner-controlled circular probe (4 mm diameter, 0.2 μm displacement resolution)
- Measured: distributed load detection, resistance-change-to-load sensitivity, spatial resolution (1.5 mm transducer spacing)
- Characterized dynamic performance: frequency response, sensitivity, linearity, repeatability for pulse waveform fidelity

---

## Key Results

- Demonstrated reliable arterial pulse signal acquisition at radial and carotid arteries
- Characterized sensor performance across multiple physiological conditions
- Validated results in human subject studies

---

## Publications

- Rahman, M.M. et al. (2025). *An Analytical Model of Motion Artifacts — Part I: Accelerometers and PPG Sensors.* **Sensors**, 25(18), 5710. [DOI](https://doi.org/10.3390/s25185710)
- Rahman, M.M. et al. (2025). *An Analytical Model of Motion Artifacts — Part II: Tactile Sensors.* **Sensors**, 25(18), 5700. [DOI](https://doi.org/10.3390/s25185700)

---

## Skills Demonstrated
`Microfabrication` `Photolithography` `PDMS` `Thin-film deposition` `PCB Design` `KiCad` `LabVIEW` `Analog circuits` `Sensor characterization`

---

[← Back to Research Portfolio](./README.md) | [→ Project 2](./project2_motion_artifact_modeling.md)
