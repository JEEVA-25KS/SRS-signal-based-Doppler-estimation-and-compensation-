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
---
## Architecture

<img width="540" height="720" alt="image" src="https://github.com/user-attachments/assets/391f63a3-32fa-4fbf-bd94-ca9e5ee09a3b" />

-----------------------------------------------------------
## Observations

- Estimated Doppler values are **very small (≈ 0 Hz)**  
  *(e.g., 0.94 Hz, 0.73 Hz)*  
- Values are **stable with minimal variation**  
- Compensation effect is **limited under current setup**  

### Reason

- Experiments conducted in an **indoor environment**  
- **No high-mobility scenarios** (UE mostly static/slow)  
- **Short UE–gNB distance** and controlled conditions  

Result: **Negligible Doppler shift observed**
