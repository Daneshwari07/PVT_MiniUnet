# PVT-MiniUNet: Lightweight Transformer for Colon Polyp Segmentation

## 📌 Overview
**PVT-MiniUNet** is a lightweight deep learning framework for **colon polyp segmentation** in colonoscopy images, designed for **resource-constrained clinical environments**.  
The model combines the **global context modeling capability of Pyramid Vision Transformer v2 (PVTv2)** with the **spatial refinement strength of a Mini-UNet decoder** to achieve accurate and efficient segmentation.

This work is an enhanced and simplified variant of the **Polyp-PVT** architecture, optimized for improved boundary preservation and reduced computational complexity.

---

## 🧠 Key Contributions
- ✔️ Replaced the **Similarity Aggregation Module (SAM)** with a lightweight **Mini-UNet decoder**
- ✔️ Improved **boundary detection** using **Camouflage Identification Module (CIM)**
- ✔️ Effective multi-scale feature fusion using **Cascaded Fusion Module (CFM)**
- ✔️ Maintains high segmentation accuracy with **lower model complexity**
- ✔️ Suitable for **real-time clinical deployment**

---

## 🏗️ Architecture
The proposed PVT-MiniUNet architecture integrates a Transformer-based encoder with a lightweight convolutional decoder to achieve accurate and efficient colon polyp segmentation.

<p align="center">
  <img src="images/model_architecture.png" alt="PVT-MiniUNet Architecture" width="800">
</p>

**Figure:** Overall architecture of the proposed PVT-MiniUNet model consisting of a PVTv2 encoder, Cascaded Fusion Module (CFM), Camouflage Identification Module (CIM), and a lightweight Mini-UNet decoder.
The proposed architecture consists of:

(Transformer-based multi-scale feature extractor)
- **Modules:**
  - Cascaded Fusion Module (CFM)
  - Camouflage Identification Module (CIM)
- **Decoder:** Lightweight **Mini-UNet**
- **Output:** Binary segmentation mask of colon polyps

---

## 📊 Dataset
- **Dataset:** Kvasir-SEG  
- **Images:** 1,000 colonoscopy images  
- **Ground Truth:** Pixel-level segmentation masks  
- **Split:**  
  - 80% Training  
  - 20% Validation  

---

## 📈 Performance
Evaluation on the **Kvasir-SEG dataset**:

| Metric | Score |
|------|------|
| Dice Coefficient | **0.9550** |
| IoU | **0.9158** |
| Parameters | **25.14M** |
| GMACs | **10.15** |

The model outperforms the baseline Polyp-PVT while maintaining efficiency.

---

## ⚙️ Training Details
- **Loss Function:** Structure-aware weighted binary cross-entropy
- **Learning Rate Scheduler:** Cosine annealing
- **Optimization Objective:** Accurate boundary preservation and stable convergence

---

## 🩺 Clinical Significance
- Enables **early detection of precancerous polyps**
- Robust against **low contrast**, **camouflaged boundaries**, and **noise**
- Practical for **real-time and low-resource clinical systems**

---

## 📁 Project Structure
PVT_MiniUnet/
│
├── Minor_Final_PolyPVT4.ipynb
├── README.md

---

## 📚 References
- Dong et al., *Polyp-PVT: Polyp Segmentation with Pyramid Vision Transformers*, 2023  
- Ronneberger et al., *U-Net: Convolutional Networks for Biomedical Image Segmentation*, 2015  
- Jha et al., *Kvasir-SEG Dataset*, 2019  

---

