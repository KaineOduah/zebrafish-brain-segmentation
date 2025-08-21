# Zebrafish Brain Segmentation (U‑Net)

**Author:** [KaineOduah](https://github.com/KaineOduah)

**Summary.** U‑Net (ResNet‑34 encoder, ImageNet‑initialized) for semantic segmentation of zebrafish brain sections. The pipeline aligns image–mask pairs, applies augmentation, trains for **200 epochs**, and evaluates on a **4-image** test split.

## Snapshot
- Data: **19** pairs (TIFF/PNG), resized to **256×1024**
- Train/Test: **15 / 4**
- Loss/Opt: **DiceLoss (binary)**, **Adam (lr=1e-4)**
- Augs: Horizontal/Vertical flips (p=0.5), Rotate ±30°, Normalize, Resize 256×1024
- Device: **Tesla T4 (CUDA)**

## Results (test set)
- IoU: 65.98%
- Accuracy: 93.28%
- Precision: 77.25%
- Recall: 81.88%
- F1 Score: 79.50%

> Metrics correspond to the run summarized in the notebook.
