# TB-FusionAI: Multimodal Deep Learning for Tuberculosis Profiling

**AI for Healthcare Mini Project | Fourth-Year B.E. | Artificial Intelligence & Data Science**  
**Rizvi College of Engineering, University of Mumbai | Academic Year 2026–2027**

## Project Overview

TB-FusionAI explores a multimodal AI framework for tuberculosis (TB) profiling by combining chest X-ray imaging with patient clinical metadata. The report describes a visual feature stream using MobileNetV3, a clinical feature stream using a multilayer perceptron (MLP), late feature fusion, and Grad-CAM for model interpretability.

> **Implementation note:** This repository contains the submitted report and the provided notebook as-is. The notebook's saved outputs show TB dataset inspection and preprocessing, plus additional analysis using a separate chest X-ray pneumonia dataset. The report's claimed multimodal MDR/XDR evaluation should not be treated as reproduced by the notebook unless that evaluation is implemented and rerun with verified resistance labels.

## Project Objectives

- Inspect and preprocess TB chest X-ray DICOM images.
- Audit clinical metadata and check whether explicit MDR, PRE-XDR, and XDR labels are available.
- Explore image preprocessing, image properties, and deep visual features.
- Document a multimodal architecture that combines image and clinical representations.
- Explore explainability through Grad-CAM as described in the report.

## Repository Contents

| File / Folder | Description |
|---|---|
| `README.md` | Project overview and repository guide |
| `AIHminiProjectReport.pdf` | Submitted project report |
| `AIH_PROJECT.ipynb` | Jupyter/Google Colab notebook with saved outputs |
| `screenshots/` | PNG images extracted from the notebook's saved visual outputs |

## Dataset

The notebook references the Kaggle dataset:

- **TB dataset:** [`raddar/drug-resistant-tuberculosis-xrays`](https://www.kaggle.com/datasets/raddar/drug-resistant-tuberculosis-xrays)
- The notebook records 1,047 DICOM image files and a metadata CSV with 1,050 rows and six columns.
- The notebook's metadata audit reports that the available CSV does not contain explicit MDR/PRE-XDR/XDR resistance labels.

The notebook also downloads a separate dataset for pneumonia analysis:

- **Pneumonia dataset:** [`paultimothymooney/chest-xray-pneumonia`](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)

These are distinct datasets and should not be presented as a single TB drug-resistance dataset.

## Technologies Used

- Python
- Google Colab / Jupyter Notebook
- PyTorch and Torchvision
- MobileNetV3
- Pandas and NumPy
- OpenCV and Pillow
- pydicom
- scikit-learn
- Matplotlib and Seaborn
- kagglehub

## How to Run

1. Open `AIH_PROJECT.ipynb` in [Google Colab](https://colab.research.google.com/) or Jupyter Notebook.
2. Run the cells in order, checking the dataset paths and output messages.
3. Allow the notebook to install its required Python packages.
4. Ensure Kaggle dataset access is available in the runtime.
5. Review the output images, plots, and dataset-audit messages.

**Important:** The notebook downloads datasets at runtime. Do not upload the full datasets to GitHub unless you have checked their license, size, and sharing terms. The notebook may require adjustments to run in a fresh environment because package versions and dataset paths can change.

## Screenshots

The following images are extracted from the notebook's saved outputs. They are illustrative outputs from the existing notebook, not proof of a completed MDR/XDR classifier.


### TB chest X-ray sample images

![TB chest X-ray sample images](screenshots/cell-21-output-02.png)

### TB X-ray preprocessing

![TB X-ray preprocessing](screenshots/cell-22-output-01.png)

### Image resolution distribution

![Image resolution distribution](screenshots/cell-23-output-03.png)

### Pixel intensity distribution

![Pixel intensity distribution](screenshots/cell-24-output-01.png)

### Brightness versus contrast

![Brightness versus contrast](screenshots/cell-32-output-01.png)

### CLAHE visualization

![CLAHE visualization](screenshots/cell-33-output-02.png)

### PCA projection of deep features

![PCA projection of deep features](screenshots/cell-35-output-01.png)

### Deep feature correlation heatmap

![Deep feature correlation heatmap](screenshots/cell-36-output-01.png)

### Image feature similarity matrix

![Image feature similarity matrix](screenshots/cell-37-output-01.png)

## Reported Results

The report states that the multimodal configuration achieved 88.6% accuracy and an 88.5% F1-score. These are **report-reported figures**; the notebook outputs currently available in this repository do not independently establish that the MDR/XDR multimodal evaluation was reproduced.

The notebook also includes a separate MobileNetV3 + Logistic Regression experiment on the pneumonia dataset, whose saved classification report shows 77.5% accuracy for NORMAL versus PNEUMONIA. This is a different task and must not be confused with MDR/XDR classification.

## Limitations and Next Steps

- Obtain verified resistance labels from a suitable source before training or evaluating MDR/XDR classification.
- Implement and save the full image-only, clinical-only, and multimodal model training/evaluation workflow if those results are required.
- Verify that screenshots and reported metrics correspond to the final notebook run.
- Avoid presenting synthetic or unverified labels as clinical ground truth.
- This academic project is not a medical diagnostic device and should not be used for clinical decisions.

## Project Team

- Ghori Daniyal Mohammed Nadeem — 19
- Shaikh Mohammed Zohair Islam — 58
- Ansari Mohammed Asif Muslim — 08
- Ansari Gulam Rabbani Qayyum — 01

**Project Guide:** Prof. Sayali Salkade  
**Department:** Artificial Intelligence & Data Science Engineering  
**Institute:** Rizvi College of Engineering, University of Mumbai
