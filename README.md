# Smart-Connected-Devices
# Predictive Maintenance – Vibration Anomaly Detection (Smart Sensor)

A proof-of-concept Industrial IoT project that detects abnormal vibration patterns in rotating machines using high-frequency acceleration data, FFT-based spectral analysis, and anomaly detection logic (distance-based or autoencoder). When an anomaly is detected, the system triggers a visual alarm and sends status data wirelessly to a dashboard.

Built as part of the Smart Connected Devices / Smart Manufacturing project track.

---

## 📌 Project Goal

Design and implement a smart vibration sensor system that:

- Samples Z-axis vibration data at ≥ 1 kHz
- Converts time-domain signals to frequency spectrum using FFT
- Learns a baseline “normal” vibration signature
- Detects abnormal patterns using:
  - Euclidean distance **or**
  - Autoencoder reconstruction error
- Triggers an LED or software flag on anomaly detection
- Sends data wirelessly to a dashboard
- Stores measurement data for later analysis

---

## 🧱 System Overview

Sensor → MCU (STM32) → Signal Conditioning → FFT → Feature Extraction →  
Anomaly Detection → Alarm (LED/Flag) → Wireless → Dashboard/Database

---

## 🛠 Hardware

- STM32 Nucleo-144 microcontroller
- Vibration / accelerometer sensor (Z-axis)
- Sensor expansion board
- OLED/LCD display (optional visualization)
- LED indicator (alarm output)
- SD card or flash storage
- Test rotating machine (fan or motor)
- Prototype wiring / PCB (project dependent)

---

## 💻 Software & Tools

- MATLAB
- Simulink
- STM32CubeIDE (or equivalent)
- DSP libraries (CMSIS-DSP or Simulink generated code)
- Git for version control

---

## 🔬 Signal Processing Pipeline

- High-frequency sampling (≥1 kHz)
- Optional filtering and windowing
- Fast Fourier Transform (FFT)
- Spectrum feature extraction
- Baseline signature capture
- Distance or reconstruction-error scoring
- Threshold-based anomaly decision

---

## 🧠 Detection Methods

### Distance-Based
Compares live spectrum to baseline spectrum using Euclidean distance.  
Triggers anomaly if distance exceeds threshold.

### Autoencoder-Based (Optional)
Model learns normal spectrum patterns and flags anomalies based on reconstruction error.

---

## 🧪 Testing Strategy

- Synthetic signal FFT validation
- Baseline capture under normal operation
- Fault injection (simulated imbalance)
- Unit tests for FFT correctness
- Integration tests: sensor → FFT → detection → alarm
- Site Acceptance Test (SAT) with defined pass/fail criteria

---

## 📊 Expected Outputs

- Frequency spectrum plots
- Baseline signature profile
- Anomaly score values
- LED alarm trigger
- Dashboard visualization
- Stored vibration datasets

---

## 📂 Repository Structure


