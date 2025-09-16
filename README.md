# Solar-Power-Plant-Deployment-in-INDIA-Strategic Solar Deployment in India: Leveraging Machine Learning for Site Localization

👨‍💻 Author
Bunyad Chaudhary – www.linkedin.com/in/bunyad-chaudhary-730854280

This repository contains the implementation and supporting material for the research paper:

Strategic Solar Deployment in India: Leveraging Machine Learning for Site Localization
<br>
Main Author: Bunyad Chaudhary
<br>
Accepted at the 16th International Conference on Computing, Communication and Networking Technologies (ICCCNT 2025), IIT Indore, India.

📌 Project Overview

India’s rapid growth in energy demand calls for scalable, efficient, and sustainable solar energy deployment. However, existing site selection methods often suffer from:

✅ Subjectivity – GIS-AHP/MCDM approaches depend on manual weightings.

✅ Opacity – Black-box ML models provide little interpretability for policymakers.

✅ Narrow scope – Many studies neglect demand-side factors like population and energy consumption.

This project proposes a fully data-driven, interpretable framework that integrates environmental, technical, and demographic criteria to rank Indian states and union territories for solar power plant deployment.

By combining autoencoder-based feature extraction, K-Means clustering, and a predicate-driven ranking system, we deliver both statistical rigor and policy-friendly insights.

🎯 Objectives

Develop a transparent and scalable methodology for solar site localization.

Balance supply-side resources (irradiance, solar potential, wind speed) with demand-side needs (population, consumption).

Use machine learning (autoencoders + clustering) to extract hidden structures in the data.

Provide interpretable outputs that policymakers, investors, and researchers can rely on.

Create a replicable framework adaptable to other countries and renewable energy domains.

📊 Dataset

A five-year dataset (2019–2023) was compiled across 29 Indian states and 8 union territories.

Features considered:

🌞 Solar Irradiance (GHI, W/m²) – sunlight availability.
🔋 Solar Potential (MW) – maximum estimated generation capacity.
⚡ Energy Consumption (kWh per capita) – demand-side requirement.
👥 Population Density – electricity distribution and demand load.
💨 Wind Speed (m/s) – secondary environmental impact on solar efficiency.

The dataset underwent:
Data cleaning (removal of missing values).
Normalization using StandardScaler.
Latent feature extraction with an Autoencoder to reduce noise and overfitting.

🧠 Methodology

1. Data Preprocessing
Normalized features to eliminate scale bias.
Handled missing values using imputation.

2. Autoencoder for Feature Extraction
Architecture: Input → Hidden Layers → 2D Latent Space → Decoder.
Trained for 50 epochs using SGD optimizer.
Captured nonlinear patterns and temporal interactions missed by PCA.

3. Clustering (K-Means + Elbow Method)
Determined optimal k = 4 using the Elbow Method.
Grouped states based on energy-environmental similarity.
Visualized results with Parallel Coordinate Plots.

4. Predicate-Driven Ranking
Defined low, medium, high thresholds for each parameter (based on statistical distribution).
Example:
GHI < 642.2 → Low | 642.2–824.6 → Medium | >824.6 → High
Wind Speed < 3.76 → Favorable | >5.38 → Unfavorable
Counted satisfied predicates → assigned categories:

⭐ Most Favorable (5/5 predicates)

🔴 Highly Favorable (4/5)

🟠 Moderately Favorable (3/5)

🟡 Favorable (2/5)

🟤 Less Favorable (1/5)

⚪ Least Favorable (0/5)

5. Visualization & Insights
Correlation Heatmaps showed strong links (Population ↔ Energy Consumption, r=+0.79).
Cluster Plots revealed groupings of high vs. low solar potential states.
Ranking Map (color-coded by category) provided quick decision support.

🏆 Key Findings

Most Favorable States (5/5): Rajasthan, Gujarat, Maharashtra
High GHI, high solar potential, strong demand, low wind speed.

Highly Favorable States (4/5): Karnataka, Tamil Nadu, Andhra Pradesh, Telangana
Robust solar potential and demand, with manageable environmental trade-offs.

Moderately Favorable (3/5): Madhya Pradesh, Uttar Pradesh, Odisha, Chhattisgarh
Potential for community solar grids with policy support.

Favorable/Less Favorable: Bihar, Kerala, Jharkhand, West Bengal
Limited irradiance/land, but good for rooftop solar and microgrids.

Least Favorable: Meghalaya, Nagaland, Arunachal Pradesh
Challenged by cloud cover, low irradiance, poor grid connectivity.
Suitable for off-grid portable solar and microgrids.

🚀 Getting Started
1. Clone Repository
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

2. Install Dependencies
pip install numpy pandas scikit-learn matplotlib seaborn

3. Run Notebook
jupyter notebook prac_mini_pro.ipynb
