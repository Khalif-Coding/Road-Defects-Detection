# 🚧 Road Defect Detection via CNN Transfer Learning (DenseNet121 & MobileNetV2)

## 📂 Repository Outline

```
RoadDefects-Detection
│
├── /RoadDefects # Original dataset folder
├── /RoadDefectsNew # Processed / reorganized dataset
│
├── P2G7_Inference.ipynb # Inference & demo notebook
├── P2G7_Khalif.ipynb # Model training & evaluation
├── README.md # Documentation
```

---

## 📌 Problem Background
**Artificial Neural Network – Computer Vision: Detecting Road Damages**

Road damage—such as **cracks**, **potholes**, **patches**, and **surface defects**—is a serious issue in many countries, including Indonesia. Damaged roads not only create discomfort for motorists, but also increase the risk of traffic accidents, slow down logistics distribution, and raise vehicle maintenance costs.

In Indonesia, with a vast road network and dense traffic, maintenance is often performed **manually**: officers must patrol, inspect, record issues, and report them. This approach is time-consuming, costly (due to delayed responses), and difficult to apply consistently across large areas.  
By applying **Computer Vision** to detect road defects, authorities can automate inspection, enable earlier detection, improve public safety, and reduce operational costs.

**Stakeholders / Users**
- Ministry of Public Works and Housing (Kementerian PUPR)  
- PT KAI (Indonesian Railways)  
- Local Governments (Pemerintah Daerah)

**Benefits (translated)**
- Automatic road inspection (**Infrastructure Maintenance**)  
- Early detection to prevent accidents and improve public safety (**Safety Assurance**)  
- Reduced manual inspections and lower maintenance costs (**Cost Efficiency**)  

**Justification**
- https://otomotif.kompas.com/read/2024/01/25/092200115/jalan-rusak-di-indonesia-kerap-jadi-penyebab-kecelakaan-dan-kemacetanr  
- https://dprd.jemberkab.go.id/jalan-berlubang-di-kecamatan-jenggawah-telah-memakan-korban-komisi-c-dprd-jember-segera-panggil-dinas-terkait/  
- https://kumparan.com/kumparannews/sederet-kasus-kecelakaan-di-jakarta-akibat-jalan-berlubang-200XyFG9Mqp

---

## 🎯 Project Output
- Trained **CNN** models using **Transfer Learning**: **DenseNet121** and **MobileNetV2**  
- **Streamlit** deployment on **Hugging Face Spaces** for real-time image classification  
- Inference notebook for testing single images and batches  

---

## 📊 Data
- **Dataset Link:** [Kaggle – Road Defects (Non-Augmented)](https://www.kaggle.com/datasets/patelmihir/road-defects-nonaugmented)  
- **Size:** ~400 images across **4 classes**  
- **Classes:** Crack, Pothole, Patch, Surface Defects  
- **Format:** Image files (JPG/PNG), organized by class folders  

---

## ⚙️ Method
- Deep Learning **CNN** with **Transfer Learning**  
- Backbones: **DenseNet121**, **MobileNetV2**  
- Training & validation on non-augmented dataset (option to extend with augmentation)  
- Deployed as a **Streamlit** app on **Hugging Face** for public inference  

---

## 🛠️ Tech Stacks

### 🔹 Languages
- Python  
- Pandas  
- SQL  
- YAML  

### 🔹 Tools
- Visual Studio Code  
- Jupyter Notebook  
- Streamlit  
- Hugging Face Spaces  
- Git & GitHub  
- Kaggle  

### 🔹 Libraries
```python
import os
import numpy as np
import pandas as pd
from PIL import Image
import matplotlib.pyplot as plt

import tensorflow as tf
from tensorflow.keras import layers, models
from tensorflow.keras.applications import DenseNet121, MobileNetV2
from tensorflow.keras.preprocessing.image import ImageDataGenerator

from sklearn.metrics import classification_report, confusion_matrix

import streamlit as st
```


## 📖 References
- [Info Kompas](https://otomotif.kompas.com/read/2024/01/25/092200115/jalan-rusak-di-indonesia-kerap-jadi-penyebab-kecelakaan-dan-kemacetanr)
- [Korban Jalan Rusak](https://dprd.jemberkab.go.id/jalan-berlubang-di-kecamatan-jenggawah-telah-memakan-korban-komisi-c-dprd-jember-segera-panggil-dinas-terkait/)
- [Korban Jalan Lubang](https://kumparan.com/kumparannews/sederet-kasus-kecelakaan-di-jakarta-akibat-jalan-berlubang-200XyFG9Mqp)

