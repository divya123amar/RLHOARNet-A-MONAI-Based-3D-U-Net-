# RLHOARNet: A MONAI-Based 3D U-Net with Lightweight Residual Boundary Refinement for Multi-Modal Brain Tumor Segmentation

## Overview

RLHOARNet (Residual Learning with Higher-Order Attention and Refinement Network) is a deep learning framework for automatic brain tumor segmentation from multi-modal MRI scans. The model extends a MONAI-based 3D U-Net architecture with a lightweight residual boundary refinement module (RLHOARBlock) to improve tumor boundary delineation while maintaining computational efficiency.

## Features

- MONAI-based 3D U-Net backbone
- Lightweight RLHOARBlock for boundary refinement
- Multi-modal MRI processing (FLAIR, T1, T1ce, T2)
- BraTS 2020 dataset support
- Dice Loss with background exclusion
- AdamW optimizer with gradient clipping
- End-to-end training and inference pipeline

## Dataset

This work uses the BraTS 2020 dataset.

Dataset Link:
https://www.med.upenn.edu/cbica/brats2020/data.html

Required files for each patient:

```
BraTS20_Training_xxx_flair.nii
BraTS20_Training_xxx_t1.nii
BraTS20_Training_xxx_t1ce.nii
BraTS20_Training_xxx_t2.nii
BraTS20_Training_xxx_seg.nii
```

## Environment

- Python 3.10+
- PyTorch
- MONAI
- NumPy
- NiBabel
- Matplotlib
- Pandas
- Scikit-learn

Install dependencies:

```bash
pip install monai nibabel numpy pandas matplotlib scikit-learn torch torchvision
```

## Repository Structure

```
RLHOARNet/
│
├── MONAI (9).ipynb
├── README.md
├── figures/
├── results/
└── trained_models/
```

## Running the Code

Open and execute:

```bash
MONAI (9).ipynb
```

or run the notebook in Google Colab/Jupyter Notebook.

## Experimental Settings

| Parameter | Value |
|------------|--------|
| Dataset | BraTS 2020 |
| Input Size | 128×128×128 |
| Modalities | FLAIR, T1, T1ce, T2 |
| Optimizer | AdamW |
| Learning Rate | 1e-4 |
| Batch Size | 1 |
| Epochs | 50 |
| Loss Function | Dice Loss |
| Framework | MONAI |

## Results

| Metric | Value |
|----------|---------|
| Mean DSC | 0.887 |
| HD95 | 4.73 mm |
| Inference Time | 2.7 sec/volume |



## Author

Divyashree A  
Research Scholar  
Alliance University, Bengaluru, India

## License

This project is intended for academic and research purposes.
