
### 🧠 Multimodal Sentiment Analysis

This project tackles **multiclass sentiment classification (Positive = 1, Negative = 2, Neutral = 0)** by **fusing four physiological and behavioral modalities**:

* **EEG** – frequency bands, engagement metrics
* **GSR** – skin conductance responses
* **Facial Action Units (TIVA)** – AU intensity/occurrence
* **Self-reports (PSY/SELFREPORT)** – subjective valence & arousal ratings

The aim is to explore and compare **baseline machine-learning models, late-fusion strategies, and advanced multimodal transformers** for robust affective computing.

---

#### 🔑 Key Features

* **Preprocessing & Synchronization**: Align EEG, GSR, and facial features using task timestamps.
* **Feature Engineering**: Bandpower, frontal asymmetry, SCR peaks, AU-based valence/arousal mapping.
* **Modeling**

  * Baseline ML (Logistic Regression, Random Forest, XGBoost)
  * Late fusion of unimodal classifiers (majority voting, stacking, weighted averaging)
  * Multimodal transformers with cross-modal attention.
* **Evaluation**: Accuracy, Macro-F1, Precision/Recall, Cohen’s Kappa, SHAP/feature importance, transformer attention visualization.
* **Experiments**: Modality ablation, binary vs 3-class setup, temporal smoothing, multitask learning, data augmentation.

---

#### 📂 Repository Structure

```
project/
├── data/                  
├── notebooks/             
│   ├── 01_preprocessing.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_modeling_baseline_sentiment.ipynb
│   ├── 04_modeling_fusion.ipynb
│   ├── 05_modeling_transformers.ipynb
│   └── 06_analysis.ipynb
├── models/               
└── README.md              
```

---

#### 🚀 Getting Started

1. **Clone** the repository

   ```bash
   git clone https://github.com/<your-username>/multimodal-sentiment-analysis.git
   ```
2. **Install** dependencies

   ```bash
   pip install -r requirements.txt
   ```
3. **Run** the notebooks sequentially or jump to specific modeling stages.

---

#### 🧪 Next Steps

* Extend with real-time inference pipeline.
* Explore additional physiological signals or language data for richer context.

---

> **Purpose**: Provide a reproducible framework for **multimodal affect recognition**, enabling researchers and practitioners to benchmark classical, fusion, and transformer-based approaches.
