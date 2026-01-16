# Estimating Causal Effects on Myocardial Infarction (MI) Risk

## Project Overview
This research explores the causal relationships between various lifestyle and medical interventions and the risk of Myocardial Infarction (MI). By moving beyond traditional regression, this project utilizes **Causal Forests** to identify **Heterogeneous Treatment Effects (HTE)**, revealing how different population subgroups respond to specific interventions.

##  Key Insights
* **Synergistic Effects:** Pharmacological interventions (statins + BP meds) combined with weight management were substantially more effective than any single treatment, achieving an **Average Treatment Effect (ATE) of -2.81**.
* **Personalized Healthcare:** Identified that patients with hypertension or high cholesterol benefit most from specific combinations of BP meds and statins.
* **Counterintuitive Findings:** Discovered that certain partial interventions (e.g., lifestyle changes alone) offered minimal impact unless paired with medication.

## Technical Implementation
* **Model Architecture:** Implemented the **CausalForestDML** estimator from Microsoft's **EconML** library.
* **Confounder Control:** Used **Propensity Score Estimation** via logistic regression and evaluated covariate balance using Standardized Mean Differences (SMD).
* **Multi-Treatment Modeling:** Modeled 31 different treatment configurations, including single, pairwise, and full combinations of five main interventions.
* **Double Machine Learning (DML):** Employed a Random Forest Regressor for the outcome model and Logistic Regression for the treatment model.

## Tech Stack
* **Languages:** Python (Google Colab)
* **Libraries:** EconML, Scikit-learn, Pandas, NumPy
* **Techniques:** Causal Inference, Double Machine Learning, Feature Engineering (Interaction Features)
