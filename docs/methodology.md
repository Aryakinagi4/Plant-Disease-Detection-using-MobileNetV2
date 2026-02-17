# Detailed Methodology

## Data Collection
Images captured using Samsung Galaxy S10 (12MP) in controlled lighting.
Initial images: 300
After cleaning: 287
After augmentation: 1152

## Preprocessing
- Noise removal
- Image resizing to 224x224
- Data augmentation:
  - Rotation
  - Inversion
  - Occlusion

## Training Details
- Architecture: MobileNetV2
- Transfer learning from ImageNet
- Optimizer: SGD
- Learning rate: 0.01
- Epochs: 50 (early stopped at 15)
- Loss function: Categorical Crossentropy

## Deployment
- Converted to TensorFlow Lite
- Integrated into Android application
