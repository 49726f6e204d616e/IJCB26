<p align="center">
  <img src="assets/attack_samples.png" width="800" alt="RF Attack Overview">
  <h1 align="center">Spectral Vulnerability: Physical RF Attacks on Face Recognition backbones</h1>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Conference-IJCB%202026%20Submission-blue">
  <img src="https://img.shields.io/badge/Python-3.9+-green">
  <img src="https://img.shields.io/badge/Hardware-Signal%20Generator-orange">
  <img src="https://img.shields.io/badge/License-MIT-lightgrey">
</p>

---

## 📌 Abstract
This repository contains the official implementation for our IJCB 2026 submission. We investigate the impact of near-field Magnetic (H) perturbations on facial recognition models. Specifically, we demonstrate how high-frequency oscillations (11.65 MHz) injected via loop antennas introduce spectral artifacts that disproportionately affect lightweight architectures like **GhostFaceNet** compared to high-capacity models like **Buffalo_L (ResNet-50)**.

## 🧪 Key Findings
| Model | Params | Susceptibility | Primary Vulnerability |
| :--- | :--- | :--- | :--- |
| **Buffalo_L** | 25.5M | **Low** | High capacity learns redundant robust features. |
| **GhostFaceNet** | 5.2M | **High** | DFC Attention and "Ghost" modules propagate noise. |

## 🖼️ Visual Analysis
### Time-Domain vs Frequency-Domain Impact
Below is the FFT analysis of a clean sample versus a physically attacked sample. Notice the distinct spectral spikes in the mid-frequency range.

<p align="center">
  <img src="assets/fft_analysis.png" width="600">
  <br>
  <i>(a) Clean FFT, (b) Physical Attack FFT, (c) Modeled Attack FFT</i>
</p>

---

## 🚀 Getting Started

### 1. Requirements
- Linux / Windows / macOS
- Python 3.9+
- CUDA (optional, but recommended)

### 2. Installation
```bash
git clone [https://github.com/YourAnonUser/Project.git](https://github.com/YourAnonUser/Project.git)
cd Project
pip install -r requirements.txt
