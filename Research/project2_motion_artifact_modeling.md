[project2_motion_artifact_modeling.md](https://github.com/user-attachments/files/27613830/project2_motion_artifact_modeling.md)
# Project 2: Motion Artifact Modeling & Time-Frequency Analysis

## Overview

Developed and validated an analytical model of motion artifacts in measured arterial pulse signals, challenging the adequacy of existing removal algorithms and proposing novel Time-Frequency Analysis approaches.

---

## Motivation

Motion artifacts (MAs) in wearable physiological sensors are typically treated as simple baseline drift — additive, low-frequency noise that can be removed with standard filtering. This project challenged that assumption fundamentally. By modeling the sensor-tissue-artery system as a mechanical 1DOF system with prestress-dependent parameters, I demonstrated that MAs generate **time-varying system parameters** — not just additive noise — making the signal inherently non-stationary and rendering conventional removal algorithms inadequate.

---

## What I Did

### Analytical Modeling
- Developed a **tissue-contact-sensor 1DOF mechanical model** incorporating:
  - Mass, stiffness, and damping of overlying tissue
  - Prestress effects on mechanical system parameters
  - Coupling between sensor contact force and arterial pulse signal
- Demonstrated mathematically that MAs produce:
  - Additive baseline drift (BD)
  - **Time-varying amplitude in each harmonic** of the measured signal
  - Non-flat harmonic-MA-coupled baseline
- Showed this "harmonic smearing" effect makes the measured signal fundamentally non-stationary

### Signal Processing Algorithms
Developed two novel Time-Frequency Analysis (TFA) algorithms:
- **Algorithm 1**: Masking signal-based EMD + HVD
- **Algorithm 2**: Complex Demodulation (CDM) + HVD

Both algorithms extract instantaneous frequency, amplitude, and phase for each harmonic component of the arterial pulse signal.

### MATLAB Implementation
- FFT-based harmonic identification
- Iterative masking signal construction and EMD decomposition
- Complex demodulation with frequency shifting
- Hilbert Vibrational Decomposition (HVD) for instantaneous parameter estimation
- ODE45-based numerical validation

### Clinical Validation
- Conducted **IRB-approved studies** (IRB24-166; IRB #19-04-FB-0100)
- Healthy participants and cardiac rehabilitation patients
- Sensor placement at radial and carotid arteries

---

## Key Findings

> *Motion artifacts do not simply add noise — they alter the mechanical system parameters of the sensor-tissue interaction, generating time-varying behavior that current removal algorithms are theoretically inadequate to handle.*

- Current wavelet, EMD, and CSE-based MA removal algorithms assume additive noise — this assumption is shown to be incorrect
- The analytical model accurately predicts observed signal variability
- The proposed TFA algorithms successfully extract beat-to-beat instantaneous parameters

---

## Publications

- **Rahman, M.M.** et al. (2025). *Motion Artifacts At-Rest in Measured Arterial Pulse Signals: Time-Varying Amplitude in Each Harmonic and Non-Flat Harmonic-MA-Coupled Baseline.* **Biosensors**, 15(9), 578. [IF ≈ 5.6; Q1] [DOI](https://doi.org/10.3390/bios15090578)
- **Rahman, M.M.** et al. (2025). *An Analytical Model of Motion Artifacts — Part I.* **Sensors**, 25(18), 5710. [DOI](https://doi.org/10.3390/s25185710)
- **Rahman, M.M.** et al. (2025). *An Analytical Model of Motion Artifacts — Part II.* **Sensors**, 25(18), 5700. [DOI](https://doi.org/10.3390/s25185700)
- **Rahman, M.M.** et al. (2020). *Improved Vibration-Model-Based Analysis for Estimation of Arterial Parameters.* ASME IMECE 2020. [DOI](https://doi.org/10.1115/IMECE2020-24551)

---

## Skills Demonstrated
`MATLAB` `ODE45` `FFT` `EMD` `HHT` `HVD` `CDM` `Signal processing` `Mechanical modeling` `IRB research`

---

[← Project 1](./project1_microfluidic_sensor.md) | [→ Project 3](./project3_bmi_clinical_study.md)
