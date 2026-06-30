# 🌙 Learning-Based Low-Light Image Denoising and Enhancement

M.Sc. Thesis — University of Padova, Italy
**Author:** Esraa Al-Najjar | **Supervisor:** Prof. Pietro Zanuttigh | Sep 2021 – Apr 2023

📄 **[Read the full thesis (PDF)](https://thesis.unipd.it/retrieve/25eb5c01-9a21-41bf-b667-87a87a70a025/Alnajjar_Esraa.pdf)**

---

## 📋 Overview

Images captured under low-light conditions suffer from severe noise, loss of detail, and poor contrast — a common challenge in surveillance, mobile photography, and autonomous systems. This thesis investigates a **two-stage deep learning pipeline** that first removes sensor noise and then enhances visibility, producing results that are both cleaner and more visually faithful than single-stage approaches.

## 🎯 Objectives

- Design a denoising stage robust to the heavy sensor noise present in extreme low-light images
- Compare multiple enhancement strategies for restoring brightness and contrast without introducing artifacts
- Evaluate restoration quality using standard image fidelity metrics, beyond visual inspection alone

## 🛠️ Methodology

**Stage 1 — Denoising**
A **ResUNet** architecture (residual learning + encoder-decoder design) was used to suppress sensor noise while preserving fine spatial details — residual connections help the network retain high-frequency structure that standard encoder-decoder models tend to lose.

**Stage 2 — Enhancement**
The denoised output was passed through three enhancement strategies, compared systematically:
- **Histogram Equalization** — traditional baseline
- **Zero-DCE** — lightweight CNN that estimates pixel-wise tonal curves for dynamic range adjustment
- **MIRNet** — multi-scale architecture that preserves high-resolution spatial context

**Dataset:** LoL (Low-Light) benchmark dataset
**Evaluation Metrics:** PSNR, SSIM

## 🔑 Key Findings

- The two-stage pipeline (denoise → enhance) consistently outperformed single-stage enhancement applied directly to noisy images
- **Zero-DCE achieved the best overall performance**, balancing visual quality with computational efficiency — a notable result given its lightweight design compared to MIRNet
- Residual connections in the denoising stage were critical for preserving structural detail in heavily degraded regions

## 🧰 Tools & Frameworks

`Python` `TensorFlow` `PyTorch` `ResUNet` `Zero-DCE` `MIRNet` `OpenCV`

## 📬 Contact

**Esraa Al-Najjar**
ML & AI Researcher | Aspiring Data Scientist
[LinkedIn](https://linkedin.com/in/esraa-al-najjar-697b39149)
