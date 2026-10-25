# 🌪️ AI/ML-Based Tropical Cyclone Identification and Classification

## 📌 Project Overview

This project focuses on developing an Artificial Intelligence (AI) and Machine Learning (ML)-based system for identifying and classifying tropical cyclone patterns using satellite imagery.

The system aims to classify tropical cyclones into different intensity categories using deep learning techniques. It explores multi-source satellite data, feature extraction, feature fusion, and attention mechanisms to improve cyclone image analysis.

## 🎯 Objectives

- Identify tropical cyclone patterns from satellite imagery.
- Classify cyclones based on their intensity.
- Explore multi-source satellite data for cyclone analysis.
- Implement a deep learning model using CNN-based feature extraction.
- Apply multi-level feature fusion and attention mechanisms.
- Evaluate model performance using standard classification metrics.
- Visualize important image regions using Grad-CAM.
- Explore future extensions for cyclone intensity and track prediction.

## 🛰️ Dataset

The project is intended to use historical tropical cyclone satellite observations from the **NOAA HURSAT-B1 dataset**.

Dataset source: [NOAA HURSAT-B1](https://www.ncei.noaa.gov/products/hurricane-satellite-data)

The planned classification categories are:

| Class | Wind Speed |
|---|---|
| Tropical Depression | Below 34 knots |
| Tropical Storm | 34 to below 64 knots |
| Hurricane/Typhoon | 64 knots or above |

**Note:** Correct classification requires reliable wind-speed labels associated with the satellite observations. The dataset must be downloaded and prepared before model training.

## 🧠 Proposed Model

The proposed architecture is called **MLFF-CycloneNet**.

Its main components include:

- **CNN Feature Extraction:** Extracts visual patterns from satellite images.
- **Multi-Level Feature Fusion:** Combines features from different network levels.
- **Attention Mechanism:** Helps the model emphasize relevant image features.
- **Classification Layer:** Predicts the cyclone intensity category.

A separate binary cyclone detector may be incorporated to distinguish cyclone images from non-cyclone images, depending on the implementation.

## ⚙️ Technologies Used

- Python
- Google Colab
- PyTorch
- Torchvision
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Seaborn
- NOAA HURSAT-B1 satellite data

## 🔄 Project Workflow

1. Collect and prepare satellite observations.
2. Preprocess images and associated labels.
3. Divide the dataset into training, validation, and testing sets.
4. Extract image features using CNN layers.
5. Fuse multi-level features and apply attention.
6. Train the model using labeled cyclone observations.
7. Predict cyclone intensity categories.
8. Evaluate classification performance.
9. Visualize model predictions and relevant image regions using Grad-CAM.

## 📊 Evaluation Metrics

The model can be evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

Grad-CAM can also be used to visualize the regions that influence the model's predictions.

Actual evaluation results should be added after running the model on the test dataset.

## 📁 Suggested Project Structure

```text
Tropical-Cyclone-Classification/
│
├── README.md
├── notebooks/
│   └── Tropical_Cyclone_Classification.ipynb
├── models/
│   └── model_weights.pth
├── results/
│   ├── confusion_matrix.png
│   └── gradcam_visualization.png
└── requirements.txt
```

*This is a suggested structure. Include only the files and folders that exist in your actual repository.*

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Open the project

Navigate to the cloned repository or upload the notebook to Google Colab.

### 3. Install dependencies

```bash
pip install torch torchvision scikit-learn matplotlib seaborn pandas numpy pillow tqdm
```

### 4. Prepare the dataset

Download the satellite data and organize the images and labels according to the notebook's expected format.

### 5. Run the notebook

Open `Tropical_Cyclone_Classification.ipynb` in Google Colab and execute the cells in order.

Configure the dataset path before starting training.

## ⚠️ Limitations

- Model performance depends on dataset quality, class balance, and label accuracy.
- The system requires suitable labeled satellite observations for reliable classification.
- Performance on unseen cyclones and satellite sources must be evaluated.
- Grad-CAM provides visual explanations but does not prove that the model's predictions are scientifically correct.
- Future cyclone-track and intensity forecasting requires additional temporal observations and dedicated prediction models.

## 🔮 Future Scope

- Integrate multiple satellite channels and data sources.
- Improve performance using larger and more diverse datasets.
- Develop time-series models for cyclone intensity forecasting.
- Explore cyclone-track prediction using historical observations.
- Build a user-friendly interface for satellite image analysis.
- Investigate near-real-time cyclone monitoring.

## 👥 Applications

- Tropical cyclone monitoring and analysis
- Weather research
- Satellite image classification
- Disaster preparedness research
- AI-assisted meteorological analysis

## 📚 References

1. NOAA National Centers for Environmental Information — HURSAT-B1 Satellite Data.
2. PyTorch Documentation: https://pytorch.org/docs/
3. Scikit-learn Documentation: https://scikit-learn.org/stable/
4. Selvaraju et al., *Grad-CAM: Visual Explanations from Deep Networks via Gradient-Based Localization*, ICCV 2017.

## 📜 Disclaimer

This project is intended for academic and research purposes. Its predictions should not be used as a substitute for official meteorological forecasts or emergency warnings.

---

**Project:** AI/ML-Based Tropical Cyclone Identification and Classification  
**Domain:** Artificial Intelligence, Deep Learning, Satellite Image Analysis
