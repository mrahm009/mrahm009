[project4_accelerometer_carotid.md](https://github.com/user-attachments/files/27613851/project4_accelerometer_carotid.md)
# Project 4: Accelerometer-Based Carotid Arterial Pulse Acquisition

## Overview

Designed a custom flexible PCB integrating analog and digital accelerometers for carotid arterial wall acceleration capture, developed analog front-end signal conditioning circuitry, and conducted an IRB-approved feasibility study evaluating accelerometer performance for arterial pulse acquisition.

---

## Motivation

Accelerometers offer a low-cost, easily miniaturized alternative to microfluidic tactile sensors for wearable cardiovascular monitoring. However, the carotid arterial pulse signal presents a significant signal conditioning challenge: the true arterial pulse amplitude is only **20–30 mV peak-to-peak** riding on top of an approximately **2V DC offset** from the accelerometer output. This project investigated whether analog and digital accelerometers could reliably capture a clear carotid arterial pulse signal prior to committing to a full-scale performance study.

---

## Hardware Design

### Custom Flexible PCB
- Integrated **ST Microelectronics analog accelerometer (LIS344ALH)** for 3-axis carotid arterial wall acceleration capture
- Subsequently integrated **digital accelerometer (LIS2DW12)** for comparison
- Designed for skin-conformable, medical-tape-fixation deployment at the neck

### Analog Front-End (AFE) Circuitry
The key engineering challenge: remove a **2V DC offset** without introducing **phase delay** that would distort pulse timing for PWV calculation.

**Solution developed:**
- Op-amp-based signal conditioning to extract the true arterial pulse signal (APG) from raw accelerometer output
- DC offset removal without phase delay introduction
- Amplification stage for signal conditioning
- NI DAQ digitization with real-time LabVIEW monitoring
- MATLAB post-processing for physiological parameter extraction

---

## Feasibility Study (IRBnet #1744951-11)

### Protocol
- Single-visit feasibility study
- Carotid pulse signals measured at **four anatomical sites** per participant:
  - Proximal and distal to the head
  - Left and right sides
- **3 repeated 1-minute recordings** per site per accelerometer
- Simultaneous brachial blood pressure and heart rate reference measurements (Mindray)

### Comparison
- Analog (LIS344ALH) vs. digital (LIS2DW12) accelerometer performance
- Identical measurement sites under medical-tape fixation
- Inter-site transit time estimation for local PWV calculation

---

## Key Findings

Identified fundamental limitations of accelerometer-based carotid pulse sensing:

1. **Tape-fixation motion coupling** — mechanical coupling between tape fixation and accelerometer introduces motion artifacts
2. **Low signal-to-noise ratio** at the neck surface
3. **DC offset instability** under varying contact pressure

> These findings directly informed the analytical motion artifact framework subsequently published in **Sensors 2025 Part I**, establishing the theoretical basis for why these limitations are fundamental rather than engineering oversights.

---

## Publication

- **Rahman, M.M.** et al. (2025). *An Analytical Model of Motion Artifacts in a Measured Arterial Pulse Signal — Part I: Accelerometers and PPG Sensors.* **Sensors**, 25(18), 5710. [DOI](https://doi.org/10.3390/s25185710)

---

## Skills Demonstrated
`Flexible PCB design` `Analog front-end circuits` `Signal conditioning` `DC offset removal` `LabVIEW` `MATLAB` `IRB research` `Human subject studies` `Accelerometer integration`

---

[← Project 3](./project3_bmi_clinical_study.md) | [← Back to Research Portfolio](./README.md)
