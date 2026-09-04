# 🌱 Robust and Explainable Lightweight Deep Learning Framework for Cross-Dataset Plant Disease Detection

## 📌 Overview

This repository contains the implementation of a lightweight deep learning framework for plant disease detection under real-world conditions.

The project focuses on cross-dataset generalization, robustness against image perturbations, and explainable AI using Grad-CAM.

## 🎯 Objectives

* Develop a lightweight plant disease detection model
* Evaluate cross-dataset generalization
* Analyze domain-shift between controlled and real-world images
* Evaluate robustness under brightness variation, Gaussian noise, and blur
* Apply Grad-CAM for model explainability
* Investigate lightweight models for mobile and edge deployment

## 📊 Datasets

### PlantVillage

PlantVillage is used for model training and validation.

* 38 disease/plant classes
* Controlled image conditions
* Used for training and validation

### PlantDoc

PlantDoc is used as an unseen real-world test dataset.

* Real-world field images
* Different backgrounds, lighting, and image conditions
* Used for cross-dataset evaluation

## 🧠 Model

### MobileNetV3-Small

MobileNetV3-Small is used as the lightweight deep learning model because of its efficient architecture and suitability for resource-constrained devices.

## ⚙️ Methodology

```text
PlantVillage Dataset
        ↓
Preprocessing
        ↓
Data Augmentation
        ↓
MobileNetV3-Small Training
        ↓
Validation
        ↓
Best Model Selection
        ↓
Unseen PlantDoc Dataset
        ↓
Cross-Dataset Evaluation
        ↓
Robustness Testing
        ↓
Grad-CAM Explainability
```

### Preprocessing

* Image resizing to 224 × 224
* Normalization
* Class mapping
* Duplicate handling
* Class balancing

### Data Augmentation

* Random Resized Crop
* Random Horizontal Flip
* Random Rotation
* Color Jitter
* Gaussian Blur
* Gaussian Noise

## 📈 Results

### PlantVillage

| Metric              |            Result |
| ------------------- | ----------------: |
| Training Images     |            43,444 |
| Validation Images   |            10,861 |
| Classes             |                38 |
| Model               | MobileNetV3-Small |
| Training Epochs     |                10 |
| Training Accuracy   |            99.82% |
| Validation Accuracy |            99.71% |

### PlantDoc

| Metric                | Result |
| --------------------- | -----: |
| Test Images           |    236 |
| Evaluated Images      |    227 |
| Correct Predictions   |     39 |
| Incorrect Predictions |    188 |
| Accuracy              | 17.18% |
| Weighted Precision    | 0.1978 |
| Weighted Recall       | 0.1718 |
| Weighted F1           | 0.1528 |
| Macro Precision       | 0.1846 |
| Macro Recall          | 0.1649 |
| Macro F1              | 0.1425 |

The large performance gap between PlantVillage validation and PlantDoc testing indicates a significant domain-shift and cross-dataset generalization problem.

## 🛡️ Robustness Evaluation

The model is evaluated under different image perturbations:

* Brightness Variation
* Gaussian Noise
* Blur

These experiments measure how model performance changes under realistic image degradation.

## 🔍 Explainable AI

Grad-CAM is used to visualize the image regions that contribute to the model's predictions.

The explainability analysis helps determine whether the model focuses on relevant plant and disease regions or is influenced by irrelevant background information.

## 💻 Installation

```bash
git clone https://github.com/YOUR-USERNAME/Plant-Disease-Detection.git
cd Plant-Disease-Detection
pip install -r requirements.txt
```

## 🚀 Usage

### Train the model

```bash
python src/train.py
```

### Evaluate the model

```bash
python src/evaluate.py
```

### Run robustness evaluation

```bash
python src/robustness.py
```

### Generate Grad-CAM explanations

```bash
python src/gradcam.py
```

## 🛠️ Technologies

* Python
* PyTorch
* Torchvision
* MobileNetV3-Small
* NumPy
* Pandas
* Scikit-learn
* Matplotlib
* OpenCV
* Grad-CAM
* Jupyter Notebook
* Kaggle

## 🔮 Future Work

* Domain adaptation
* Improved data augmentation
* Test-Time Augmentation (TTA)
* Domain generalization
* Model quantization
* Knowledge distillation
* Mobile and edge deployment
* Advanced explainability techniques

## 👨‍💻 Author

**Salman Al Mahmud**

**Wasik Imam**

BSc in Computer Science and Engineering

East Delta University

## 📚 Thesis

**A Robust and Explainable Lightweight Deep Learning Framework for Cross-Dataset Plant Disease Detection under Real-World Conditions**
