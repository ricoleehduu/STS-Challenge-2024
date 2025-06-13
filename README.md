# 🦷 STS 2024: 2nd Semi-supervised Teeth Segmentation MICCAI Challenge  
**MICCAI 2024, Marrakesh, Morocco | October 6-10, 2024**  

---

## 📌 Introduction  
The **STS 2024 Challenge** focuses on advancing semi-supervised learning for tooth segmentation in dental imaging. We extend the 2023 challenge to multi-instance and multi-class settings, emphasizing instance-level segmentation. This year features two tracks:  
- **2D Panoramic X-ray Segmentation**  
- **3D Dental CBCT Segmentation**  

Our goal is to address the limitations of labeled data in dental imaging while balancing segmentation accuracy, inference speed, and GPU resource efficiency.  

![image-20250613133108457](C:\work\2025-05-13\code\STS-Challenge-2024\assets\image-20250613133108457.png)

---

## 🗓️ Important Dates (PST)  
> ⚠️ *Note: Dates are currently unavailable in this format. Please refer to the official website for updates.*  

---

## 📊 Evaluation Metrics  
Results are evaluated using a **multi-metric framework** to balance accuracy and efficiency:  
- **Region error**: Dice Similarity Coefficient (DSC), Intersection over Union (IoU)  
- **Boundary error**: Normalized Surface Dice (NSD)  
- **Instance-level detection**: Identification Accuracy (IA)  
  - IA = `#{D ∩ G} / #{D ∪ G}` (via Mask IoU ≥ 0.5 matching)  
- **Efficiency**: Running Time (RT), GPU Memory-Time Area (GPU-area)  

For implementation details, visit our [evaluation code repository](https://github.com/STS-challenge/STS).   

---

## 📈 Ranking Scheme  
1. Compute **image-level metrics** (DSC, IoU, NSD)  
2. Calculate **instance-level metrics** (DSC, IoU, NSD, IA) via greedy matching  
3. Measure **RT and GPU-area** (final testing phase only)  
4. Rank teams separately by each of the 9 metrics  
5. Final rank = average of 9 ranks (ties allowed)  

---

## 🏆 Challenge Awards  
- **Cash Prize**: $500 for 1st place  
- **Certificates**: Top 10 teams  
- **Oral Presentation**: Invitations for top performers  
- **Paper Publication**: Workshop paper opportunities for outstanding teams  

---

## 🏁 Tracks  

### Track 1: 2D Panoramic X-ray Segmentation  
**Goal**: Segment 32 permanent teeth (including wisdom teeth) and 20 deciduous teeth.  

![image-20250613132918804](C:\work\2025-05-13\code\STS-Challenge-2024\assets\image-20250613132918804.png)
**Join here**: [CodaBench Competition](https://www.codabench.org/competitions/3024/#/pages-tab)   

### Track 2: 3D Dental CBCT Segmentation  
**Goal**: Segment 32 permanent teeth in 3D CBCT scans.  

![image-20250613132935913](C:\work\2025-05-13\code\STS-Challenge-2024\assets\image-20250613132935913.png)
**Join here**: [CodaBench Competition](https://www.codabench.org/competitions/3025/#/pages-tab)   

---

## 🏅 Final Results  
### Panoramic X-ray Track  

![image-20250613133002565](C:\work\2025-05-13\code\STS-Challenge-2024\assets\image-20250613133002565.png)

### CBCT Track  
![image-20250613133020574](C:\work\2025-05-13\code\STS-Challenge-2024\assets\image-20250613133020574.png)

---

## 📁 Repository Structure  
```bash
STS2024-Challenge/  
├── README.md               # This file  
├── assets/                 # Store competition images here  
│   ├── panoramic_segmentation.png  
│   ├── cbct_segmentation.png  
│   ├── panoramic_winners.png  
│   └── cbct_winners.png  
└── evaluation_code/        # Official evaluation scripts (link to GitHub)  