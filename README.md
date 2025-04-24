# 🧠 MMRML: EEG Microstate-Based Machine Learning for Dementia Detection

This repository contains the official implementation of the research paper:

**“Mapping the Mind at Rest: Machine‑Learning Identification of Alzheimer’s and Frontotemporal Dementia through EEG Microstate Parameters”**  
📄Authors: Kazi Abrar Shafin, Md Maruf Imtiaz, Rabbi Al Nahiyan, Raiyan Rahman, Mahdy Rahman Chowdhury

---

## 🧠 Overview

Dementia—including Alzheimer’s Disease (AD) and Frontotemporal Dementia (FTD)—affects millions worldwide. This project explores the use of **EEG microstate analysis**, a non-invasive and cost-effective method, to classify AD, FTD, and healthy controls using machine learning.

We leverage:

- EEG signal processing
- Microstate segmentation using GFP peaks and modified K-means
- Feature extraction (GEV, Duration, Occurrence, etc.)
- ML classification (SVM, etc.)
- Explainable AI (SHAP) for insights

📊 **Achieved a classification accuracy of 97.05% in the Beta band using SVM**

---

## 📂 Dataset

We use publicly available EEG data sourced from the [OpenNeuro repository](https://openneuro.org/), specifically:

- **Dataset Title**: _Resting-State EEG in Alzheimer's Disease and Frontotemporal Dementia_
- **Subjects**: 60 individuals total
  - 30 Alzheimer's Disease (AD) patients
  - 15 Frontotemporal Dementia (FTD) patients
  - 15 Healthy Controls (HC)
- **Data Format**: `.set` files (EEGLAB format)
- **Channels**: 64-channel EEG
- **Duration**: 5-minute resting-state (eyes-closed)

🔗 **Note**: Due to licensing and privacy concerns, raw EEG data is not included in this repository. You must download it manually from OpenNeuro and place it in the `data/` folder as per folder structure.

---

## 🖼️ Visualizations

| EEG Microstates                        | SHAP Interpretability            | Model Performance                      |
| -------------------------------------- | -------------------------------- | -------------------------------------- |
| ![Microstates](images/microstates.png) | ![SHAP](images/shap_summary.png) | ![Accuracy](images/model_accuracy.png) |

<!-- <sub>📌 Visuals will be added soon. Place your images in the `images/` directory.</sub> -->

---

## 🛠️ Features

- EEG signal preprocessing and bandpass filtering
- Microstate segmentation using Global Field Power (GFP)
- Modified K-means clustering for 4-state model
- 6 microstate features: Duration, Occurrence, Coverage, GEV, Transition Probability, Mean Map
- ML classification: SVM, kNN, Random Forest
- Explainable AI using SHAP values

---

## 📁 Folder Structure

```
MMRML/
├── data/                 # EEG dataset (download manually)
├── preprocessing/        # Filtering and artifact removal
├── microstate_analysis/  # GFP peak detection, clustering
├── features/             # Microstate parameter extraction
├── classification/       # ML model training & evaluation
├── explainability/       # SHAP analysis scripts
├── images/               # Plots and result figures
├── results/              # Accuracy, logs, CSVs
└── README.md             # This file
```

---

## 📊 Results

| Classifier   | Accuracy (Beta Band) |
| ------------ | -------------------- |
| SVM          | **97.05%**           |
| RandomForest | 94.88%               |
| kNN          | 90.76%               |

---

<!-- ## 📚 Citation

```bibtex
@article{shafin2025mapping,
  title={Mapping the Mind at Rest: Machine-Learning Identification of Alzheimer's and Frontotemporal Dementia through EEG Microstate Parameters},
  author={Shafin, Kazi Abrar and Imtiaz, Md Maruf and Nahiyan, Rabbi Al and Rahman, Raiyan and Chowdhury, Mahdy Rahman},
  journal={Elsevier Preprint},
  year={2025}
}
```

--- -->

## 👥 Contributors

- Kazi Abrar Shafin
- Md Maruf Imtiaz
- Rabbi Al Nahiyan
- Raiyan Rahman
- Mahdy Rahman Chowdhury

---

## 📬 Contact

📧 For questions, reach out via email: **mahdy.chowdhury@northsouth.edu**
