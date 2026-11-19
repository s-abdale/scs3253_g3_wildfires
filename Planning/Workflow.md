# Project Workflow
Topics: Division of work & timeline of tasks (timeline to be added after review)

Status: Proposed to team, tasks divided ✅

## Division of Work
Roles are divided into 4 technical areas.

#### Data Engineering & Pipeline
* **Responsibility:** Owning the data ingestion and cleaning pipeline.
* **Tasks:**
  * Pulling and filtering the NASA FIRMS (fire data) and NASA POWER (weather data) specifically for Canada.
  * Writing the script to aggregate point-based satellite data into a clean spatial-temporal grid (e.g., daily grid cells by region).
  * Handling missing values, data type conversions, and automated merging of weather and fire datasets.


#### Feature Engineering & Exploratory Data Analysis
* **Responsibility:** Transforming raw data into predictive features.
* **Tasks:**
  * Creating lag features (e.g., "what was the average temperature and precipitation over the last 7 days?").
  * Performing feature scaling, handling skewed distributions (e.g., log transformations on FRP values), and running feature selection techniques to drop noisy variables.
  * Creating correlation matrices and visual plots for the presentation.

#### Supervised Modeling — Classification & Ensembles
* **Responsibility:** Building the core classification models to predict high-risk wildfire days.
* **Tasks:**
  * Setting up the training/test splits and baseline models (Logistic Regression).
  * Training advanced ensemble models (Random Forest Classifier and Gradient Boosting from Chapters 6 & 7).
  * Evaluating models using **Precision, Recall, F1-Score, and ROC-AUC** (Chapter 3) to handle class imbalance (since severe fire days are rarer than normal days).

#### Unsupervised Clustering & App Visualizer
* **Responsibility:** Adding advanced unsupervised learning and building the user-facing web app.
* **Tasks:**
  * Implementing **K-Means or DBSCAN clustering (Chapter 9)** to group Canadian regions into behavioral climate-risk clusters and testing if adding cluster labels improves the supervised model's accuracy.
  * Building the simple HTML/JS or React app visualizer that displays the model's predictions, risk maps, or interactive weather sliders.