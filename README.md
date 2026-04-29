<p align="center">
  <img src="media/HardwareSetup.png" width="500" alt="RF Attack Overview">
  <h1 align="center">Intentional Electromagnetic Interference Attacks on Facial Recognition</h1>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Conference-IJCB%202026%20Submission-blue">
  <img src="https://img.shields.io/badge/Python-3.9+-green">
  <img src="https://img.shields.io/badge/Hardware-Signal%20Generator-orange">
</p>

---

## 📌 Abstract
Attacks on general computer vision algorithms are often relegated to the digital domain, with the optimization performed purely in the digital world and then translated to physical mediums for implementation. In the field of biometrics, including facial recognition, physical presentation attacks targeting biometric sensors are dominant and present significant opportunity and risk. This paper highlights a critical vulnerability in the physical-to-digital pipeline of biometric sensors and provides a standardized approach for testing facial recognition system robustness against hardware attacks, going beyond and potentially complementing presentation attacks (as defined in ISO/IEC 30107 standard series). Specifically, in this work we (a) demonstrate that intentional electromagnetic interference is possible to be conducted with commonly accessible radio frequency (RF) equipment, (b) assess the robustness of state-of-the-art face recognition methods against RF-based attacks, and (c) provide a dataset composed of face images captured with and without electromagnetic interference to serve as a new benchmark for testing modern face matchers against RF-sourced interference.

## 📀 Dataset
The dataset will be released if the paper is accepted. 


## 🖼️ Visual Analysis
### Time-Domain vs Frequency-Domain Impact
Below is a single identity shown without perturbations, modeled attack, and physical attack. Notice the distinct vertical lines in the attacked images, caused by the attack.

<p align="center">
  <img src="media/02463d566_clean.png" width="300">
  <img src="media/02463d566_attack_digital.png" width="300">
  <img src="media/02463d566_attack.png" width="300">
  <br>
  <i>(a) Clean Image, (b) Modeled Attack, (c) Physical Attack FFT</i>
</p>

---

## 🚀 Getting Started

### 1. Requirements
- Linux / Windows / macOS
- Python 3.9+
- CUDA (optional, but recommended)

### 2. Scripts
There are only two scripts necessary for the IEMI Modeling. 
- RF_Optimization.py: Runs a grid search over provided parameters to determine theoretically optimal RF settings per model (models built in same as IJCB paper).
- RF_effect_modeling: Using the outputs from RF_Optimization.py, the script overlays the desired RF parameters (frequency, amplitude, bar angle, AM effect, FM effect) onto a directory of images. 

### 2. Installation
```bash
git clone [https://github.com/YourAnonUser/Project.git](https://github.com/YourAnonUser/Project.git)
cd Project
pip install -r requirements.txt


