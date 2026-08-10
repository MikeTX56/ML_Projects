[![wakatime](https://wakatime.com/badge/github/MikeTX56/ML-A-to-Z.svg)](https://wakatime.com/badge/github/MikeTX56/ML-A-to-Z)
# **Machine Learning A-to-Z**

This repository documents a complete, hands-on journey through machine
learning.\
It includes small, focused projects, mathematical derivations,
experiments, and practice notebooks.\
The goal is to build a strong foundation in both the practical and
theoretical sides of machine learning.

> 📍 **Full learning path:** See [ROADMAP.md](./ROADMAP.md) — a structured,
> phase-by-phase guide covering ML/DS mastery, electronics from first
> principles, embedded ML (TinyML), and building a business around these
> skills.

------------------------------------------------------------------------

## **Repository Structure**

    ML-A-to-Z/
    │
    ├── projects/
    │   ├── classification/
    │   │   ├── churn_prediction/
    |   |   ├── crdit_card_detection/
    │   │   ├── heart_disease_prediction/
    |   |   ├── iris_classification/
    |   |   ├── mnist_classfication/
    │   │   ├── spam_detection/
    |   |   └── titanic_survivors/
    │   │
    │   ├── linear_regression/
    │   │   ├── bike_sharing/
    |   |   ├── car_price_predition/
    │   │   └── house_price_prediction/
    │   │
    │   ├── clustering/          (Phase 2 — unsupervised learning)
    │   ├── signal_processing/   (Phase 3 — DSP with Python)
    │   ├── tinyml/              (Phase 4 — embedded ML on MCUs)
    │   └── deep_learning/       (Phase 5 — CNNs, RNNs, Transformers)
    │
    ├── math/
    │   └── linear_regression/
    │       ├── normal_equation/
    │       └── SGD_and_BGD/
    │
    ├── experiments/
    │   (scratch work, quick tests, temporary notebooks)
    │
    ├── ROADMAP.md   ← start here for the complete learning path
    └── README.md

**Folder meanings:**

-   **projects/** -- complete ML projects organized by type
    (classification, regression).\
-   **math/** -- math notes and derivations for algorithms such as
    gradient descent and the normal equation.\
-   **experiments/** -- quick tests, scratch notebooks, and exploratory
    files.\
-   **each project** contains:
    -   `data/` --- datasets\
    -   `notebooks/` --- Jupyter notebooks for EDA and model building\
    -   optional `src/` for `.py` scripts

------------------------------------------------------------------------

## **Skills and Tools Used**

-   Python\
-   NumPy, pandas, Matplotlib\
-   scikit-learn\
-   Linear regression and classification models\
-   Feature engineering and preprocessing\
-   Exploratory Data Analysis (EDA)\
-   Gradient descent and related optimization concepts\
-   Git and reproducible project structure

------------------------------------------------------------------------

## **How to Use This Repository**

1.  Navigate to any project under `projects/`.\
2.  Open the `notebooks/` folder.\
3.  Run the main notebook from top to bottom.\
4.  Ensure datasets are inside the project's `data/` folder.

Each project is self-contained and can be run independently.

------------------------------------------------------------------------

## **Purpose of This Repository**

This repository tracks ongoing progress in machine learning, combining
theory and implementation.\
It serves as a learning log, a portfolio of completed work, and a
foundation for more advanced topics.

------------------------------------------------------------------------

## **Future Additions**

See [ROADMAP.md](./ROADMAP.md) for the full plan. High-level upcoming work:

-   Unsupervised learning (clustering, PCA, autoencoders)\
-   Regularization methods (Ridge & Lasso)\
-   Decision trees and ensemble models (XGBoost, LightGBM)\
-   Signal processing with Python (FFT, filters, spectrograms)\
-   TinyML / embedded ML on microcontrollers\
-   Deep learning (CNNs, RNNs, Transformers)\
-   MLOps basics (experiment tracking, model serving)\
-   Deployment examples (FastAPI, Docker)
