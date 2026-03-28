# Automated Brain Tumor Detection in MRI using Ensemble Learning and XAI

[cite_start]This project presents an automated approach for classifying brain tumors in Magnetic Resonance Imaging (MRI) scans using Convolutional Neural Networks (CNNs) and Explainable Artificial Intelligence (XAI) techniques[cite: 1, 5].

## 📋 Project Overview
[cite_start]Early and accurate detection of brain tumors is vital for clinical decision support and choosing the appropriate treatment[cite: 4]. [cite_start]This study utilizes three pre-trained architectures with **Fine-Tuning**, integrated via **Ensemble Learning** to maximize generalization and accuracy[cite: 5, 38].

## 🚀 Methodology
* [cite_start]**Dataset**: LGG MRI Segmentation (by Mateusz Buda) sourced from Kaggle[cite: 6, 59].
* [cite_start]**Architectures**: VGG16, Xception, and InceptionResNetV2[cite: 5, 43, 79].
* [cite_start]**Preprocessing**: Normalization, Data Augmentation, and class balancing[cite: 6, 77].
* [cite_start]**Data Split**: 70% Training, 20% Validation, and 10% Test[cite: 75, 76].
* [cite_start]**Interpretability**: Implementation of **Grad-CAM** (XAI) to visualize the regions influencing the models' decisions[cite: 9, 44, 171].

## 📊 Performance Results
[cite_start]The **Ensemble Learning** approach (Arithmetic Mean Voting) achieved the best overall performance[cite: 8, 164, 256]:

| Model | Accuracy | Recall | F1-Score | AUC |
| :--- | :---: | :---: | :---: | :---: |
| InceptionResNetV2 | 0.88 | 0.86 | 0.87 | 0.952 |
| VGG16 | 0.90 | 0.89 | 0.89 | 0.961 |
| Xception | 0.91 | 0.89 | 0.90 | 0.968 |
| **Ensemble (Final)** | **0.93** | **0.92** | **0.92** | **0.979** |

[cite_start]*Note: Results obtained on the test set after Fine-Tuning[cite: 267, 272].*

## 🧠 Explainability (XAI)
[cite_start]By applying **Grad-CAM**, heatmaps were generated to highlight the most relevant areas for prediction[cite: 9, 172]. [cite_start]This visual validation ensures the models are focusing on the actual tumor regions, increasing the reliability of the clinical results[cite: 174, 314, 333].

## 🛠️ Usage
1.  Clone the repository.
2.  Install dependencies: `pip install -r requirements.txt`.
3.  [cite_start]Automate the dataset download using the `kagglehub` library as implemented in the notebook[cite: 60].
4.  Run the `Relatorio_DL_Trabalho_P3.ipynb` notebook.

## 📜 License
This project is licensed under the MIT License - see the `LICENSE` file for details.

---

### Pro-Tip for your Portfolio:
Would you like me to help you write a **LinkedIn post** in English to share this new repository? It’s a great way to show your network that you're working with high-level AI!
