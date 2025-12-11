# 🌸 Any-Sensor Edge Vision Robustness

**Team:** RobustaVision  
**Team Members:** 221236 Islombek Abdurakhmanov || 220724 Odilova Zulayho || 221011 Jabborova Amina  
**Course:** Computer Vision (Fall 2025)  
**Supervisors:** Dr. I. Atadjanov & Dr. B. Kiani  
**GitHub:** islombek-cs/RobustaVision

---

## 📘 Abstract

This project explores **robust computer vision models** capable of maintaining accuracy under variable **sensor conditions** such as low resolution, compression, motion blur, or frame rate drops.

We propose a lightweight **degradation-aware adapter** module that enhances the robustness of pretrained CNN or ViT models for edge devices.

---

## 🔧 Problem & Motivation

Edge devices often capture **degraded visual data**.

Standard CNNs fail under blur, noise, compression, or lighting changes.

Our goal: build an efficient model that **adapts dynamically** to degradation.

---

## 📚 Related Work

- **DeepAugment / AugMix** – improve data diversity for robustness.  
- **Adapters / LoRA** – lightweight fine-tuning layers for pretrained models.  
- **ImageNet-C / CIFAR-C** – standardized corruption benchmarks.

---

## 🗂️ Data & Resources

**Datasets:**

- CIFAR-10, CIFAR-10-C  
- (Optional) ImageNet-C subset  

**Frameworks:** PyTorch, TorchVision, NumPy, Matplotlib  
**Hardware:** Google Colab GPU (T4 / A100)

---

## 🧠 Method Overview

1. **Input:** Corrupted images (blur, noise, compression)  
2. **Base Model:** Pretrained ResNet18  
3. **Adapter:** Lightweight correction module  
4. **Training:** Mix clean + corrupted samples  
5. **Evaluation:** Compute clean vs. corrupted accuracy  

---

## 📊 Evaluation Metrics

| Metric          | Description                                  |
|-----------------|----------------------------------------------|
| Clean Accuracy  | Accuracy on normal test set                  |
| Robust Accuracy | Avg. accuracy across CIFAR-C corruptions     |
| Corruption Gap  | Clean − Robust accuracy                      |
| Inference Time  | Latency on edge device                       |

---

## ⚠️ Risks & Mitigations

| Risk               | Mitigation                       |
|--------------------|-----------------------------------|
| High training cost | Use CIFAR-10-C                    |
| Poor generalization| Apply AugMix                      |
| Limited GPU        | Use Colab with low batch size     |

---

## 🗓️ Timeline

| Week | Task                           |
|------|--------------------------------|
| W1   | Dataset setup, literature review |
| W2   | Implement base ResNet model      |
| W3   | Add adapter module               |
| W4   | Train and evaluate on CIFAR-C    |
| W5   | Plot results and visualize       |
| W6   | Write final report               |

---

## 🎯 Expected Outcomes

- Robust classification under real-world distortions.  
- Deployable on low-power edge hardware.  
- Open-source code and reproducible experiments.

---

## ⚖️ Ethics & Compliance

- Uses open datasets only.  
- No personal or biometric data.  
- Pretrained models credited under MIT license.

---

## 📚 References

1. Hendrycks et al., “Benchmarking Neural Network Robustness to Common Corruptions and Perturbations,” ICLR 2019  
2. Rusak et al., “A Simple Way to Make Neural Networks Robust Against Diverse Image Corruptions,” CVPR 2021  
3. Zhang et al., “LoRA: Low-Rank Adaptation for Efficient Fine-Tuning,” ICLR 2022  
4. Xu et al., “DeepAugment: Mixing Multiple Corruption Spaces,” NeurIPS 2021  
