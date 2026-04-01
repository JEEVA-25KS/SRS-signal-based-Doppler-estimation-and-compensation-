# SRS based Doppler Estimation and Compensation Framework for OAI 5G gNB

## Overview
This project presents a **real-time Doppler estimation and compensation framework** integrated into the OpenAirInterface (OAI) 5G gNB.

In high-mobility scenarios, Doppler shifts introduce:
- Carrier frequency offset (CFO)
- Inter-carrier interference (ICI)
- Degraded link performance

To address this, the framework implements a **cross-layer solution**:
- **MAC Layer → Doppler Estimation (using SRS)**
- **PHY Layer → Doppler Compensation (UL + DL)**

---

## Objectives
- Estimate **per-UE Doppler shift** using SRS
- Apply **stable filtering for noise reduction**
- Perform:
  - Uplink frequency-domain compensation
  - Downlink time-domain pre-compensation
- Maintain **modular MAC–PHY architecture**

---

## Core Idea

Doppler is estimated using phase change between consecutive SRS signals:
<img width="183" height="110" alt="image" src="https://github.com/user-attachments/assets/863e67be-2574-4ee5-8c91-ef320f9acf00" />
Doppler is estimated using phase change between consecutive SRS signals:

