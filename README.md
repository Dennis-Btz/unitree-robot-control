# Project Description

This repository contains the deployment software for the **Unitree Go2** quadruped. It handles the Sim-to-Real transfer by executing trained DRL policies on the robot's NVIDIA Jetson Orin Nano using ONNX.

### Key Features
- [ ] **Inference Engine:**
    - [ ] Executes static computation graphs via **ONNX Runtime** (CPU-optimized) for efficient, low-latency policy evaluation.
- [ ] **Hardware Communication:**
    - [ ] Interfaces with the robot's firmware via **Unitree SDK2** and **Cyclone DDS** (LowState/LowCmd topics).
- [ ] **Real-Time Control Loop:**
    - [ ] Maintains a precise **500 Hz (2ms)** control cycle with **Trajectory Interpolation** for smooth motor commands.
- [ ] **Sim-to-Real Interface:**
    - [ ] Maps sensor data to the required 1x1x37 observation tensor and includes **Soft-Start** safety mechanisms.

### Infrastructure
- [ ] **Dependency Management:**
    - [ ] Strictly reproducible environment via **uv** and **Poetry**.
- [ ] **Compatibility:**
    - [ ] Locked to **Python 3.10** to ensure stability with hardware drivers.
- [ ] **Modular Architecture:**
    - [ ] Separates core control logic (`src/`) from network configuration scripts (`scripts/`).

### Current Status
- [ ] **Pipeline Validation:** The technical infrastructure (DDS, ONNX, Control Loop) is fully implemented.
- [ ] **Policy Deployment:** System is ready for deployment; awaiting the final converged policy.