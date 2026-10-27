# Machine Learning Based Prediction of Student Academic Performance in Open University Settings Using Online Engagement

Research project repository for the Postgraduate Diploma in Data Analytics,
The Independent Institute of Education (Emeris), November 2026.

**Student:** Nyasha Grace Manyonganise (ST10538027)
**Supervisor:** Dr Mfowabo Maphosa
**Module:** Research Project (RPDA8412)

## Study overview
This study predicts final student outcomes (successful: Pass/Distinction; adverse: Fail/Withdrawn)
in an open university setting using early online engagement and assessment data from the Open
University Learning Analytics Dataset (OULAD). Predictive performance is compared at three fixed
prediction windows (Week 2, Week 4, Week 6) using Logistic Regression, Random Forest and XGBoost.

## Repository structure
- `Python Notebooks/` – the three analysis notebooks, in execution order:
  1. `Data Preparation` – loads OULAD, validates and constructs the Week 2/4/6 analytical datasets
  2. `Exploratory Data Analysis` – target balance, missingness, distributions, correlations
  3. `Modelling` – model training, held-out evaluation, confusion matrices, feature importance
- `oulad_outputs/` – derived analytical datasets and figures produced by the notebooks
- `requirements.txt` – Python libraries required to reproduce the analysis

## How to reproduce the analysis
1. Install Python 3.10+ and run `pip install -r requirements.txt`.
2. Download the OULAD dataset from the original source (Kuzilek, Hlosta and Zdrahal, 2017,
   https://doi.org/10.1038/sdata.2017.171) or the Kaggle mirror, and place the CSV files
   in the same folder as the notebooks (do NOT place them inside this repository).
3. Run the notebooks in the order listed above. The preparation notebook writes its outputs
   to `oulad_outputs/`; the EDA and modelling notebooks read from that folder.

## Data ethics
This repository contains **derived code and analytical outputs only**. The original OULAD
dataset is not rehosted; users must obtain it from the original source. OULAD is an
anonymised dataset and the analysis does not attempt reidentification (Kuzilek, Hlosta
and Zdrahal, 2017).

## Reference
Kuzilek, J., Hlosta, M. and Zdrahal, Z., 2017. Open University learning analytics dataset.
Scientific Data, 4, article 170171.

