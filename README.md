# Smart Greenhouse - Plant Disease Detection

This repository provides a CNN-based deep learning model for classifying crop leaf images into healthy or diseased categories. The model is a core component of the "AI-Based Smart Greenhouse" project, which aims to assist aging farmers through automation and precision agriculture.

## 🔍 Purpose

Modern smart farms often manage the environment as a whole (e.g., temperature, humidity) but lack per-crop level diagnosis. Our approach supplements existing systems by:
- Installing cameras for individual plant monitoring
- Detecting disease symptoms on leaves in real time
- Reducing labor required for visual inspection

## 🧠 Model Architecture

- **Backbone**: EfficientNetB0 with ImageNet pretrained weights
- **Pipeline**:
  - Input: 224x224 RGB images
  - Transfer learning + GlobalAveragePooling + Dense + Dropout + Sigmoid output
- **Loss**: Binary cross-entropy
- **Optimizer**: Adam
- **Metrics**: Accuracy

## 📁 Directory Layout

```
smart-greenhouse-disease-detector/
├── 이미지_분류_딥러닝_모델.py   # Training & evaluation script
└── README.md                    # Project documentation
```

## 🧪 Dependencies

```bash
pip install tensorflow matplotlib numpy
```

## 📦 Data Structure

```
/data
  ├── train/
  │   ├── healthy/
  │   └── infected/
  └── test/
      ├── healthy/
      └── infected/
```

## 🚀 Quick Start

```bash
python 이미지_분류_딥러닝_모델.py
```

- Trains the model on preprocessed dataset
- Uses data augmentation (flip, zoom, shift, etc.)
- Early stopping & model checkpointing enabled

## 📈 Evaluation

- Reports test set accuracy and loss
- Visualizes accuracy/loss per epoch
- Displays prediction results with color-coded labels (green: correct, red: incorrect)

## 🔧 Potential Improvements

- Multi-class support for more disease types
- Model quantization for edge device deployment
- Integration with real-time IoT dashboard

## 👥 Contributors

- 노경민 (단국대학교 사이버보안학과)
- 전호영 (단국대학교 사이버보안학과)

## 🏅 Background

This work was developed for the 2025 Smart Agriculture Hackathon. It contributes to sustainable farming by enabling automated, crop-specific disease detection to assist elderly farmers with limited physical capacity.
