<font size="6">**D**epth everything **M**odel **B**enchmark</font>

### Authors: Кирилин Антон, Милёшин Илья, Корнаев Алексей
### Course: Computer Vision Project 2025 (HSE University)

---

## Project Idea

### Motivation:
Classical stereo-vision approaches for depth estimation require multi-camera setups and often generate noisy results. Modern deep learning methods allow monocular depth estimation (MDE) — predicting a depth map from a single RGB image.

We aim to compare:
- Zero-shot depth estimation models (trained on diverse large datasets)  
vs  
- Classical supervised models trained specifically on a given dataset.

We want to check:
- How well universal zero-shot models generalize to unseen data.
- Whether they can outperform specialized supervised models.
- Which preprocessing techniques influence results the most.
- Whether a hybrid fine-tuned approach is necessary.

---

## Research Plan

### Selected Models:
| Model        | Type | Characteristics              |
|--------------|------|--------------------------------|
| MiDaS v3.1   | Zero-shot | Strong generalization, relative depth |
| Depth Anything | Zero-shot / Foundation | Best zero-shot depth estimation model in 2024 |
| ZoeDepth     | Hybrid | Combines relative + metric depth |
| AdaBins      | Supervised | Best indoor depth estimation model (NYUv2) |
| NeW CRFs / DPT | Supervised | Best outdoor depth estimation models (KITTI) |

---

## Selected Datasets for Evaluation:
| Dataset | Domain  | Notes |
|---------|---------|------|
| NYU Depth v2 | Indoor  | RGB-D dataset from Kinect |
| KITTI        | Outdoor | Street scenes with LiDAR ground truth |
| DIODE        | Mixed   | Indoor + Outdoor, high precision |
| ETH3D / Middlebury | Evaluation | Accurate ground truth for detail comparison |

---

## Metrics:
- AbsRel (Absolute Relative Error)
- RMSE (Root Mean Squared Error)
- δ1 (Threshold accuracy)
- Optional: Edge-based and gradient metrics.

---

## Current Implementation:
### Implemented in Google Colab:
- Automated installation of dependencies.
- Download and setup of all models via Torch Hub.
- Automatic download of NYU Depth V2 sample dataset.
- Batch inference with MiDaS, Depth Anything, ZoeDepth.
- Calculation of metrics for depth estimation.
- Visualization of results.

---

## Next Steps:
- Extend evaluation to full NYU, KITTI, DIODE datasets.
- Add fine-tuned supervised models (AdaBins, DPT KITTI).
- Aggregate all results into summary tables.
- Visual comparison of models on diverse scenes.
- Prepare a tiny-paper report for a conference or internal presentation.

---

## Repository Structure:
