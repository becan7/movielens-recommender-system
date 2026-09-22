# 🎬 CineStream Pipeline: MovieLens Data Pipeline & Recommender Engine

[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)

An end-to-end data processing pipeline, Exploratory Data Analysis (EDA), and movie recommendation engine built on top of the MovieLens dataset (+100k ratings)[cite: 1]. This repository implements automated data quality control, statistical profiling, and vector-based recommendation algorithms (Collaborative Filtering and Content-Based Filtering)[cite: 1].

---

## 📌 Project Overview

This project focuses on transforming raw user-item interaction data into actionable similarity matrices for personalized movie recommendations[cite: 1]. It handles data ingestion, quality validation, clean-up of orphan records, and feature preprocessing required for predictive modeling[cite: 1].

### Key Highlights
* **Data Quality & Validation**: Complete integrity verification across all primary tables with zero duplicate rows identified[cite: 1].
* **Exploratory Data Analysis**: Statistical profiling of user rating distribution (ranging from 0.5 to 5.0 stars) and feature coverage analysis[cite: 1].
* **Data Sanitization**: Identification and removal of 18 unrated movies to prevent sparsity anomalies in recommendation matrices[cite: 1].
* **Recommendation Architecture**: Implementation of vector similarity algorithms (`Cosine Similarity`) for item-based and collaborative recommendation models[cite: 1].

---

## 📊 Dataset Metrics

The project processes the benchmark **MovieLens Small Dataset**[cite: 1]:

| Table | Record Count | Attributes & Description |
| :--- | :--- | :--- |
| **`movies.csv`** | 9,742 | Contains movie titles, unique `movieId`, and associated genres[cite: 1]. |
| **`ratings.csv`** | 100,836 | User evaluations rated on a 0.5 to 5.0 star scale[cite: 1]. |
| **`tags.csv`** | 3,683 | User-applied metadata labels and descriptors[cite: 1]. |
| **`links.csv`** | 9,742 | Identifiers mapping titles to IMDb and TMDb records[cite: 1]. |

> ⚠️ **Data Quality Note**: EDA revealed that 8,170 movies lack user-assigned tags, and 18 titles had no ratings attached[cite: 1]. Unrated titles were filtered out during the preprocessing phase[cite: 1].

---

## 🛠️ Tech Stack

* **Core Language**: `Python 3.9+`
* **Data Processing & ETL**: `Pandas`[cite: 1], `NumPy`[cite: 1]
* **Machine Learning & Analytics**: `Scikit-Learn` (`cosine_similarity`, `train_test_split`)[cite: 1]
* **Data Visualization**: `Matplotlib`[cite: 1]
* **Development Environment**: `Jupyter Notebooks`[cite: 1]

---

## 📁 Repository Structure

```text
.
├── data/                      # MovieLens raw dataset files
├── notebooks/
│   └── eda_recommender.ipynb  # Data cleaning, EDA, and similarity matrix generation
├── README.md                  # Technical documentation
└── requirements.txt           # Project dependencies
```

---

## 🚀 Getting Started

### Prerequisites
Python 3.9 or higher and `pip` installed on your local environment.

### Installation & Execution

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/david-del-olmo/movielens-recommender-system.git](https://github.com/david-del-olmo/movielens-recommender-system.git)
   cd movielens-recommender-system
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install required packages:**
   ```bash
   pip install pandas numpy matplotlib scikit-learn jupyter
   ```

4. **Run the Jupyter Notebook:**
   ```bash
   jupyter notebook notebooks/eda_recommender.ipynb
   ```

---

## 📄 License

This project is licensed under the **MIT License** — see the `LICENSE` file for details.

---

## ✉️ Contact

**David del Olmo Otero**  
*Computer Engineering Student | Junior Backend & Data Engineer*  

* 💼 **LinkedIn**: [linkedin.com/in/david-del-olmo-otero](https://linkedin.com/in/david-del-olmo-otero)
* ✉️ **Email**: david.delolmotero@gmail.com
