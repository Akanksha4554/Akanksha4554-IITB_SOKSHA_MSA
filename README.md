
# 🌌 Multimodal Sentiment Analysis

## 🪄 What This Project Is Really About

Human emotions are messy, but our sensors capture quiet clues.
This project pulls those threads together to **classify sentiment**—**Positive (1), Neutral (0), Negative (2)**—
by combining **four very different streams of evidence**:

| Signal                     | Why We Care                                    | Sample Nuggets                              |
| -------------------------- | ---------------------------------------------- | ------------------------------------------- |
| 🧠 **EEG**                 | Brain rhythms hint at engagement and mood      | Delta–Gamma bandpower, frontal asymmetry    |
| 🌊 **GSR**                 | Tiny shifts in skin conductance reveal arousal | Mean level, number of SCR peaks             |
| 🙂 **Facial Action Units** | Micro-expressions whisper feelings             | AU12 smile, AU4 frown, AU1 brow raise       |
| ✍️ **Self-Reports**        | The participant’s own voice                    | Valence/arousal ratings mapped to sentiment |

Instead of betting on a single sensor, we **fuse them late**, stack their strengths, and
experiment with **transformer architectures** that let each modality “talk” to the others.

---

## 🔧 Key Moves

* **Time-Aligned Preprocessing** – EEG, GSR, and facial features synced to task events.
* **Feature Crafting** – From engagement indices to AU-based valence estimates.
* **Model Line-Up**

  * Classic baselines: Logistic Regression, Random Forest, XGBoost
  * Late-fusion ensembles: voting, stacking, weighted logits
  * Multimodal Transformers: cross-modal attention for deep fusion
* **Transparent Evaluation** – Macro-F1, Cohen’s Kappa, SHAP plots, attention heatmaps.

---

## 🗂 Folder Map

```
project/
├─ data/                  
├─ notebooks/              
│   ├─ 01_preprocessing.ipynb
│   ├─ 02_feature_engineering.ipynb
│   ├─ 03_modeling_baseline_sentiment.ipynb
│   ├─ 04_modeling_fusion.ipynb
│   ├─ 05_modeling_transformers.ipynb
│   └─ 06_analysis.ipynb
├─ models/                 
└─ README.md
```

---

## ⚡ Quick Start

1. **Clone the repo**

   ```bash
   git clone https://github.com/<your-username>/multimodal-sentiment-analysis.git
   cd multimodal-sentiment-analysis/project
   ```
2. **Open the notebooks**
   Each notebook is self-contained with its own imports.
   Run them in order to walk through preprocessing → modeling → analysis.
   *No global `requirements.txt` is required.*

---

## 🧪 Things to Try

* **Sensor Mix-and-Match** – Drop one modality at a time to see its real impact.
* **Binary vs. Ternary** – Compare Positive/Negative only vs. full 3-class setup.
* **Temporal Smoothing** – Track sentiment drift across a session.
* **Creative Augmentation** – GAN-generated EEG, jittered GSR, synthetic facial AUs.

---

## 🌟 Why This Repository Feels Different

* Blends **neuroscience, physiology, and behavior** in a single, reproducible pipeline.
* Clear, modular notebooks that read more like a **guided lab journal** than boilerplate code.
* Designed for curious researchers who want to **peek under the hood of human affect**.

---

