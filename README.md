# 🎵 Spotify Songs Clustering (K-Means + EDA)

This project applies **unsupervised clustering** on a dataset of the **most streamed songs in 2024**, with the goal of identifying distinct song groups based on their digital popularity metrics across multiple platforms.

> 📅 Project Date: June 2, 2025  
> 📁 Dataset: [Kaggle - Most Streamed Spotify Songs 2024](https://www.kaggle.com/datasets/nelgiriyewithana/most-streamed-spotify-songs-2024)

---

## 🧠 Objective

Group songs based on streaming behavior and platform exposure to uncover clusters such as:
- Global top hits
- Niche or emerging songs
- Explicit viral tracks
- Generic mainstream content

This analysis supports data-driven playlist curation, marketing targeting, and digital trend segmentation.

---

## 🛠️ Tools & Libraries

- **Google Colab** (Python)
- **RapidMiner Studio**
- Python: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `plotly`

---

## 📊 Dataset Description

- 4,600+ songs  
- 29 original features (platform presence, streams, track info)
- 7 selected numerical features for clustering:
  - `Track Score`
  - `Spotify Streams`
  - `Spotify Popularity`
  - `Apple Music Playlist Count`
  - `Deezer Playlist Count`
  - `Amazon Playlist Count`
  - `Explicit Track` (binary)

---

## 📈 Workflow (Python)

1. **Exploratory Data Analysis (EDA)**
   - Correlation matrix, artist frequency, distribution analysis
2. **Data Cleaning & Preparation**
   - Converted stream counts, handled missing values
3. **Feature Scaling**
   - Standardized 7 features with `StandardScaler`
4. **K-Means Clustering**
   - Used Elbow & Silhouette methods to determine `k = 4`
5. **Cluster Analysis**
   - Used `PCA` for 2D visualization
   - Summarized feature means per cluster
   - Interpreted behavioral traits of each segment

---

## 🔁 RapidMiner Replication

![RapidMiner Workflow](images/rapidminer_1.jpg)
- Identical 7-feature pipeline was implemented in RapidMiner.
- Normalization with Z-Transformation.
- K-Means with `k = 4`, results matched Python interpretation.
![Inertia Cluster](images/python_1.1.jpg)
![Silhoutte Cluster](images/python_1.2.jpg)
- Cluster model, centroid table, and line plots used for validation.

---

## 📌 Results

![Python Results](images/python_1.jpg)
![RapidMiner Results](images/rapidminer_1.1.jpg)
![RapidMiner Cluster Graph](images/rapidminer_1.2.jpg)
| Cluster | Description |
|---------|-------------|
| Cluster 0 | Average exposure songs, mid-level streams |
| Cluster 1 | Top hits with high playlist & stream count |
| Cluster 2 | Up-and-coming songs with strong Spotify metrics |
| Cluster 3 | Explicit or edgy songs with high Track Score |

---

## ✅ Conclusion

This project successfully uncovered song groupings using K-Means clustering on real-world streaming data. The dual-approach implementation in both **Python and RapidMiner** reinforces the reproducibility and interpretability of the results.

## 📎 License
This project is for academic and learning purposes. Dataset credit to [Nidula Elgiriyewithana](https://www.kaggle.com/nelgiriyewithana).
