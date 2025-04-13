# <ins>D</ins>epth anything <ins>M</ins>odel <ins>B</ins>enchmark

### Authors: Кирилин Антон, Милёшин Илья, Корнаев Алексей
### Course: Computer Vision Project 2025 (Innopolis University)

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
| [MiDaS v3.1](https://github.com/isl-org/MiDaS)   | Zero-shot | Strong generalization, relative depth |
| [Depth Anything V2](https://github.com/DepthAnything/Depth-Anything-V2) | Zero-shot / Foundation | Best zero-shot depth estimation model in 2024 |

---

## Datasets for Evaluation:
| Dataset | Domain  | Notes |
|---------|---------|------|
| NYU Depth v2 | Indoor  | RGB-D dataset from Kinect |
| KITTI        | Outdoor | Street scenes with LiDAR ground truth |
| DIODE        | Mixed   | Indoor + Outdoor, high precision |

---

## Metrics:
- AbsRel (Absolute Relative Error)
- RMSE (Root Mean Squared Error)
- δ1 (Threshold accuracy)

---

## Next Steps:
- [ ] Write a scripts for inference of DAM V2 and MiDaS v3.1
- [ ] Choose a dataset for evaluation (one or many)
- [ ] Find an appropriate architecture for supervised model
- [ ] Create a scritpt for supervised model training / inference
- [ ] Compare a supervised model performance with DAM V2 & MiDaS v3.1 ones

## Related works

- [Depth Anything V2](https://arxiv.org/abs/2406.09414)
- [Depth Anything: Unleashing the Power of Large-Scale Unlabeled Data](https://arxiv.org/abs/2401.10891)
- [MiDaS v3.1 -- A Model Zoo for Robust Monocular Relative Depth Estimation](https://arxiv.org/abs/2307.14460)

---
