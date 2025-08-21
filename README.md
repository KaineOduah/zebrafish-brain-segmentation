# Zebrafish Brain Segmentation (U‑Net)

**Author:** [KaineOduah](https://github.com/KaineOduah)

Semantic segmentation of zebrafish brain images using a **U‑Net (encoder=ResNet‑34, ImageNet weights)**. The notebook implements the full pipeline end‑to‑end: data pairing, augmentation, model training (200 epochs), and evaluation on a held‑out test split.

## Data
- **Total matched pairs:** 19 (TIFF images with PNG masks)
- **Split:** 15 train / 4 test (stratified by filename match)
- **Resize:** 256×1024 (HxW)
- **Batch size:** 4 (train), 4 (test)

## Model
- **Backbone:** U‑Net w/ **resnet34** encoder (**imagenet**)
- **Loss:** DiceLoss (binary)
- **Optimizer:** Adam (lr=1e-4)
- **Epochs:** 200
- **Threshold:** 0.5 for binarizing masks
- **Augmentations:** Horizontal/Vertical flips (p=0.5), Rotate ±30°, Normalize, Resize 256×1024
- **Hardware:** Tesla T4 (CUDA)

## Results (test set)
- **IoU:** 65.98%  
- **Accuracy:** 93.28%  
- **Precision:** 77.25%  
- **Recall:** 81.88%  
- **F1 Score:** 79.50%  

## Repository Contents
- `Final_Zebrafish_Code_SU2025.ipynb` — full code & analysis
- `docs/index.md` — short project page
- `requirements.txt`, `.gitignore`, `LICENSE`

## License
This repository uses the **MIT License**. Copyright © 2025 KaineOduah. 
The MIT license allows others to use, modify, and distribute the code (even commercially) **as long as** they keep your copyright and license notice. It also disclaims warranty/liability.
