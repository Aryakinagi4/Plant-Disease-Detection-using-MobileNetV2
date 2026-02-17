# Identification of Anthracnose in Chillies using Deep Learning on Embedded Platforms

This repository documents the research work presented in:

"Identification of Anthracnose in Chillies using Deep Learning on Embedded Platforms"
Published in: 2023 3rd International Conference on Smart Data Intelligence (ICSMDI)
IEEE Xplore: https://ieeexplore.ieee.org/document/10127878

---

## Project Overview

Chilli anthracnose, caused by the Colletotrichum fungus, significantly reduces crop yield. This research proposes a Deep Learning-based classification system to distinguish healthy and diseased chillies and deploy the model on an embedded/mobile platform.

The system uses Transfer Learning with MobileNetV2 to achieve high accuracy while maintaining a lightweight model size suitable for edge deployment.

---

## Dataset Description

Images were collected from:
- University of Agricultural Sciences, Dharwad
- Chilli farms in Kusugal (Hubli outskirts)

Classes:
- Healthy Green
- Healthy Red
- Diseased Green
- Diseased Red

Total Images (after augmentation): 1152  
Training Split: 80%  
Testing Split: 20%

### Dataset Distribution

| Class            | Training | Testing |
|------------------|----------|----------|
| Healthy Green    | 160      | 40       |
| Healthy Red      | 159      | 40       |
| Diseased Green   | 282      | 71       |
| Diseased Red     | 320      | 80       |
| **Total**        | **921**  | **231**  |

---

## Methodology

1. Image collection in controlled white-background environment
2. Manual preprocessing and noise removal
3. Data augmentation (rotation, inversion, occlusion)
4. Resizing images to 224x224
5. Transfer Learning using MobileNetV2 (ImageNet pretrained)
6. Optimization using Stochastic Gradient Descent (learning rate = 0.01)
7. Early stopping (stopped at epoch 15 out of 50)
8. Conversion to TensorFlow Lite for Android deployment

---

## Model Performance

Training Accuracy: 98.6%  
Testing Accuracy: 96.94%

### Model Comparison

| CNN Model      | Accuracy (%) | Model Size (MB) |
|---------------|-------------|----------------|
| VGG16        | 93.2        | 148            |
| ResNet50     | 95.4        | 98             |
| ResNet18     | 97.3        | 45             |
| MobileNetV2  | 96.94       | 15             |

MobileNetV2 was selected due to its optimal balance between accuracy and model size for embedded deployment.

---

## Edge Deployment

- Model converted to TensorFlow Lite (.tflite)
- Android application developed for real-time classification
- On-device inference (no cloud dependency)

---

## Key Contributions

- Custom dataset creation for Anthracnose disease
- Lightweight transfer learning pipeline
- Embedded AI deployment on Android device
- Comparative analysis of multiple CNN architectures

---

## Repository Contents

data/raw/            Raw dataset (not included)
data/processed/      Augmented dataset (not included)
results/figures/     Training graphs and visualizations
results/tables/      Performance comparison tables
docs/                Methodology explanation
paper/               Published paper

---

## Academic Citation

If you reference this work:

Kinagi et al., "Identification of Anthracnose in Chillies using Deep Learning on Embedded Platforms", ICSMDI 2023.

---

## License

This repository documents published academic research.
All rights reserved to the authors.