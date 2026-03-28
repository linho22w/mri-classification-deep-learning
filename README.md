# Automated Brain Tumor Detection in MRI using Ensemble Learning and XAI

This project presents an automated approach for classifying brain tumors in Magnetic Resonance Imaging (MRI) scans using Convolutional Neural Networks (CNNs) and Explainable Artificial Intelligence (XAI) techniques.

## 📋 Project Overview
Early and accurate detection of brain tumors is vital for clinical decision support and choosing the appropriate treatment. This study utilizes three pre-trained architectures with **Fine-Tuning**, integrated via **Ensemble Learning** to maximize generalization and accuracy.

## 🚀 Methodology
* **Dataset**: LGG MRI Segmentation (by Mateusz Buda) sourced from Kaggle.
* **Architectures**: VGG16, Xception, and InceptionResNetV2.
* **Preprocessing**: Normalization, Data Augmentation, and class balancing.
* **Data Split**: 70% Training, 20% Validation, and 10% Test.
* **Interpretability**: Implementation of **Grad-CAM** (XAI) to visualize the regions influencing the models' decisions.

## 📊 Performance Results
The **Ensemble Learning** approach (Arithmetic Mean Voting) achieved the best overall performance:

| Model | Accuracy | Recall | F1-Score | AUC |
| :--- | :---: | :---: | :---: | :---: |
| InceptionResNetV2 | 0.88 | 0.86 | 0.87 | 0.952 |
| VGG16 | 0.90 | 0.89 | 0.89 | 0.961 |
| Xception | 0.91 | 0.89 | 0.90 | 0.968 |
| **Ensemble (Final)** | **0.93** | **0.92** | **0.92** | **0.979** |

*Note: Results obtained on the test set after Fine-Tuning.*

## 🧠 Explainability (XAI)
By applying **Grad-CAM**, heatmaps were generated to highlight the most relevant areas for prediction. This visual validation ensures the models are focusing on the actual tumor regions, increasing the reliability of the clinical results.

## 🛠️ Usage
1.  Clone the repository.
2.  Install dependencies: `pip install -r requirements.txt`.
3.  Automate the dataset download using the `kagglehub` library as implemented in the notebook.
4.  Run the `brain_tumor_detection.ipynb` notebook.

## 📄 Full Academic Report
For a deep dive into the methodology, architectural choices, and comprehensive results, please read the full project report: 
[Download/View the Report (PDF)](./Relatorio_DL_Trabalho_P3.pdf) #########################

## 📜 License
This project is licensed under the MIT License - see the `LICENSE` file for details.
