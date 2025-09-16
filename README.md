# Solar-Power-Plant-Deployment-in-INDIA-Strategic Solar Deployment in India: Leveraging Machine Learning for Site Localization

👨‍💻 Author
Bunyad Chaudhary – www.linkedin.com/in/bunyad-chaudhary-730854280

This repository contains the implementation and supporting material for the research paper:

Strategic Solar Deployment in India: Leveraging Machine Learning for Site Localization
Main Author: Bunyad Chaudhary
Accepted at the 16th International Conference on Computing, Communication and Networking Technologies (ICCCNT 2025), IIT Indore, India.

The project explores data-driven solar site selection across Indian states and union territories using a custom-built dataset, autoencoder-based dimensionality reduction, clustering, and predicate-driven ranking. It provides interpretable insights for policymakers and a replicable framework for renewable energy planning.

🔑 Objectives

Identify optimal states for large-scale solar power plant deployment in India.

Move beyond subjective GIS–AHP or opaque black-box ML models by offering transparent, data-driven analysis.

Balance supply-side factors (solar irradiance, potential, wind speed) with demand-side factors (population density, energy consumption).

Provide a scalable, adaptable methodology that can be applied to other regions or renewable technologies.

📊 Dataset

A 5-year dataset (2019–2023) was curated covering 29 states and 8 union territories of India.
Features include:

🌞 Global Horizontal Irradiance (GHI, W/m²)

👥 Population Density

⚡ Energy Consumption (kWh per capita)

🔋 Solar Potential (MW)

💨 Wind Speed (m/s)

Data was normalized, pre-processed, and evaluated against statistically derived thresholds.

🧠 Methodology

Preprocessing

Data cleaning, missing value imputation, and normalization with StandardScaler.

Feature Reduction with Autoencoder

Extracted latent features from the dataset.

Reduced overfitting and captured hidden spatio-temporal interactions beyond PCA.

Clustering (K-Means + Elbow Method)

Determined optimal number of clusters.

Classified states into groups with similar energy and demographic characteristics.

Predicate-Based Evaluation

Defined quantitative ranges (low, medium, high) for each parameter.

Counted satisfied predicates per state to assign categories:

Most Favorable

Highly Favorable

Moderately Favorable

Favorable

Less Favorable

Least Favorable

Visualization

Parallel Coordinate Plots

Feature Correlation Heatmaps

State Rankings

🏆 Key Results

Most Favorable States: Rajasthan, Gujarat, Maharashtra

Highly Favorable States: Karnataka, Tamil Nadu, Andhra Pradesh, Telangana

Moderately Favorable: Madhya Pradesh, Uttar Pradesh, Odisha, Chhattisgarh

States like Bihar, Kerala, and West Bengal show potential for rooftop solar / microgrid solutions.

North-eastern states (e.g., Meghalaya, Nagaland, Arunachal Pradesh) are less favorable for large-scale projects but suitable for decentralized/off-grid innovations.

This aligns closely with India’s national solar deployment targets, while providing interpretable justifications for ranking.

🚀 Getting Started
Prerequisites

Python 3.9+

Jupyter Notebook

Required libraries:

pip install numpy pandas scikit-learn matplotlib seaborn

Running the Notebook

Clone the repository:

git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>


Launch Jupyter Notebook:

jupyter notebook prac_mini_pro.ipynb


Run all cells to reproduce analysis, visualizations, and rankings.

📂 Repository Structure
├── prac_mini_pro.ipynb    # Main implementation notebook
├── 16th_ICCCNT_2025_paper_5471.pdf   # Accepted IEEE research paper
└── README.md              # Project documentation
and many other imp files

