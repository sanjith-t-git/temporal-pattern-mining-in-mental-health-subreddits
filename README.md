# 🧠 Temporal Pattern Mining in Mental Health Reddit Data  
### Unsupervised Discovery of Depression & Anxiety Subtypes + Longitudinal Dynamics

---

## 📌 Overview

Mental health narratives are dynamic — they evolve over time, influenced by personal experiences and global events.

This project presents a **large-scale temporal mining framework** that analyzes **2.4M+ Reddit posts over 15 years (2008–2022)** to uncover:

- Latent mental health subtypes  
- Temporal evolution of emotional states  
- Behavioral transitions between psychological conditions  

Using **SBERT embeddings + UMAP + HDBSCAN**, we identify meaningful patterns in depression and anxiety narratives and analyze how they change over time.

---

## 🎯 Key Contributions

- 🧩 **Subtype Discovery**  
  Identified 10 latent mental health clusters such as Sleep Disturbance, Anxiety, Suicidal Ideation, Therapy, and Relationship Stress  

- 📈 **Temporal Analysis (15 Years)**  
  Modeled weekly evolution of mental health narratives across 778 weeks  

- 🔄 **Behavioral Transition Modeling**  
  Discovered clinically meaningful pathways:
  - Sleep → Anxiety  
  - Medication → Therapy  
  - Emotional Numbness → Suicidal Ideation  

- ⚡ **Volatility & Stability Analysis**  
  Distinguished between:
  - Stable baseline signals (Sleep, Anxiety)  
  - Episodic crisis signals (Suicidal Ideation)  

- 🌍 **Real-World Event Alignment**  
  Detected major shifts corresponding to:
  - 2016–2017 (Academic stress rise)  
  - 2020 (COVID-19 mental health impact)  

---

## 🧠 Methodology

### 🔹 Pipeline Overview

---

### 🔹 1. Data Preprocessing
- Cleaned and normalized Reddit posts  
- Removed noise (URLs, short posts, stopwords)  
- Lemmatization for semantic consistency  
- Organized into weekly time bins  

---

### 🔹 2. Sentence Embeddings (SBERT)
- Model: `all-mpnet-base-v2`  
- Output: 768-dimensional semantic embeddings  
- Captures deep contextual meaning  

---

### 🔹 3. Dimensionality Reduction (UMAP)
- Reduced embeddings to lower-dimensional space  
- Preserved semantic relationships  
- Enabled efficient clustering  

---

### 🔹 4. Clustering (HDBSCAN)
- Density-based clustering (no predefined k)  
- Robust to noise and outliers  
- Extracted **10 meaningful clusters**  

---

### 🔹 5. Temporal Pattern Mining

Performed multi-stage temporal analysis:

- 📊 Weekly prevalence tracking  
- 🔍 Change-point detection  
- 🔄 Transition dynamics  
- 🔗 Correlation & co-occurrence analysis  
- ⚡ Volatility measurement  

---

## 📊 Results & Visualizations

---

### 🧩 Cluster Visualization (UMAP Projection)

- Each point represents a Reddit post  
- Clear separation of mental health subtypes  

![UMAP Clusters](figures/umap_clusters.png)

---

### 📈 Temporal Evolution of Clusters

- Tracks how mental health themes change over time  
- Major spike observed in 2020 (COVID-19)  

![Weekly Trends](figures/weekly_prevalence.png)

---

### 🔄 Transition Dynamics

- Shows how users move between mental states  

![Transition Matrix](figures/transition_matrix.png)

---

### 🔗 Correlation Between Clusters

- Sleep ↔ Anxiety (r = 0.62)  
- Medication ↔ Therapy (r = 0.55)  

![Correlation Heatmap](figures/correlation_heatmap.png)

---

### ⚡ Volatility Analysis

- Suicidal ideation → highly volatile  
- Sleep & anxiety → stable baseline  

![Volatility Heatmap](figures/volatility_heatmap.png)

---

## 📊 Evaluation Metrics

| Metric                  | Value  |
|------------------------|--------|
| Silhouette Score       | 0.47   |
| Davies–Bouldin Index   | 0.82   |
| Calinski–Harabasz      | 312.4  |

These metrics confirm that the discovered clusters are **coherent, well-separated, and meaningful**.

---

## 🧠 Key Insights

### 1. Layered Structure of Mental Health
- **Baseline:** Sleep, Anxiety  
- **Contextual:** Academic stress, relationships  
- **Adaptive:** Therapy, coping  
- **Crisis:** Suicidal ideation  

---

### 2. Mental Health is Dynamic
- Not static categories  
- Evolves through identifiable pathways  

---

### 3. Real-World Impact
- COVID-19 caused major shifts in mental health narratives  
- Academic cycles influence stress-related clusters  

---

### 4. Clinical Relevance
- Transition patterns align with psychological progression  
- Potential for early-warning systems  

---

## 📂 Project Structure

temporal-pattern-mining-mental-health/
│
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   └── 02_temporal_pattern_mining_pipeline.ipynb
│
├── embeddings/
│   └── sbert_umap_embeddings.npy
│
├── clustering/
│   └── cluster_labels.npy
│
├── figures/
│   ├── umap_clusters.png
│   ├── weekly_prevalence.png
│   ├── transition_matrix.png
│   ├── correlation_heatmap.png
│   └── volatility_heatmap.png
│
├── requirements.txt
└── README.md

---

## 🛠️ Tech Stack

- Python  

- Sentence Transformers (SBERT)  

- UMAP  

- HDBSCAN  

- NumPy, Pandas  

- Matplotlib, Seaborn  

---

## ⚖️ Ethical Considerations

- Data is anonymized but sensitive  

- No individual-level predictions  

- Focus on population-level insights  

- Designed for **supportive, not diagnostic use**  

---

## 🚀 Future Work

- Real-time mental health monitoring systems  

- Integration with digital health platforms  

- Multimodal analysis (text + audio + physiological signals)  

- Personalized intervention strategies  

---

## 👤 Author

**Sanjith Thiruvengadam**  
