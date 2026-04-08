# 🐾 Global Mammalian Biodiversity Analysis using Machine Learning

## 📌 Project Overview
This project analyzes global mammalian biodiversity using the **Observations_Mammalia_Global dataset**. The objective is to explore spatial patterns of species distribution and apply machine learning models to predict species based on geographical coordinates (latitude and longitude).

The study combines **Exploratory Data Analysis (EDA)** with **Machine Learning techniques** to understand ecological patterns and evaluate model performance.

---

## 🎯 Objectives
- Analyze global distribution of mammalian species
- Identify spatial patterns and observation density
- Apply machine learning models for species prediction
- Compare performance of different models
- Improve model accuracy through optimization

---

## 📂 Dataset
- **Source:** iNaturalist Observations Dataset
- **File:** `observations_mammalia_global.csv`
- **Features Used:**
  - `latitude`
  - `longitude`
  - `scientific_name` (target variable)

---

## 🧹 Data Preprocessing
- Removed missing values
- Filtered invalid latitude and longitude values
- Encoded species using Label Encoding
- Reduced dataset to **top 50 most frequent species** to handle class imbalance
- Applied feature scaling using **MinMaxScaler**

---

## 📊 Exploratory Data Analysis (EDA)
The following visualizations were created:

- 📈 Top 10 Most Observed Species
- 🌍 Latitude Distribution Histogram
- 🌍 Longitude Distribution Histogram
- 📍 Species Distribution Scatter Plot
- 🔥 Observation Heatmap

These analyses revealed:
- Strong geographic clustering of species
- Sampling bias toward developed regions
- Uneven global observation distribution

---

## 🤖 Machine Learning Models

### 1. Random Forest (Primary Model)
- Handles non-linear relationships
- Works well with large datasets
- Optimized using hyperparameters

### 2. Support Vector Machine (SVM)
- Used for non-linear classification
- Trained on sampled data due to computational constraints

### 3. Linear Regression (Baseline)
- Used for comparison
- Demonstrates limitations of linear models in classification tasks

---

## ⚙️ Model Optimization
Random Forest performance was improved using:
- Increased number of estimators
- Controlled tree depth
- Adjusted splitting parameters

---

## 📈 Results

| Model | Accuracy |
|------|---------|
| Random Forest (Before Tuning) | 31.99% |
| Random Forest (After Tuning) | **41.55%** ✅ |
| SVM | ~8% |
| Linear Regression | ~0% |

---

## 🧠 Key Insights
- Species distribution is **non-linear and spatially complex**
- Random Forest performs best due to ensemble learning
- SVM performs moderately but is computationally expensive
- Linear Regression fails due to inability to model non-linearity
- Geographic coordinates alone are insufficient for high-accuracy prediction

---

## ⚠️ Limitations
- High number of classes (species)
- Class imbalance
- Limited features (only latitude & longitude)
- Sampling required due to computational constraints

---

## 🚀 Future Improvements
- Use Deep Learning (CNN, LSTM)
- Apply Graph Neural Networks (GNN)
- Include environmental features (climate, habitat)
- Improve class balancing techniques

---

##  📁 Project Structure

```
machine-learning-project1/
│
├── 📁 ShikhaPriya/                 # Folder containing visualization images
│   ├── latitude_density.jpg
│   ├── longitude_density.jpg
│
├── 📄 Priya.ipynb                 # Data analysis & preprocessing notebook
├── 📄 ShikhaPriya1019.ipynb       # Model training & evaluation notebook
│
├── 🖼️ latitude_density.jpg        # Visualization outputs
├── 🖼️ longitude_density.jpg
├── 🖼️ observation_heatmap.jpg
├── 🖼️ species_distribution.jpg
├── 🖼️ top_10_species.jpg
│
├── ⚙️ scaler.pkl                 # Saved scaler model (small file)
│
├── 📄 .gitignore                 # Ignore large files (.csv, .pkl, etc.)
├── 📄 README.md                  # Project documentation
│
└── 📄 requirements.txt           # Required libraries (optional)
```

---

# 📝 Notes

* Large files like datasets (`.csv`) and heavy models (`.pkl > 100MB`) are excluded.
* Visualizations are saved as images for easy understanding.
* Jupyter notebooks contain complete workflow:

  * Data Cleaning
  * EDA (Exploratory Data Analysis)
  * Model Training
  * Evaluation

---

# 🚀 Future Improvements

* Add API using FastAPI/Flask
* Deploy model
* Optimize model size
* Add frontend (Streamlit)

```
```



---

## 🔗 GitHub Repository
👉 https://github.com/shikhapriya1019/machine-learning-project1/tree/main

---

## 📚 Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib & Seaborn
- Scikit-learn

---

## 👩‍💻 Author
**Shikha Priya**

---

## ⭐ Conclusion
This project demonstrates the application of machine learning in biodiversity analysis. The results highlight the importance of model selection, feature engineering, and optimization in handling complex ecological datasets.
