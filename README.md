# Predicting Heart Failure Survival 
This project predicts heart failure patients’ survival and identifies the most predictive features from medical record data.\
_(Final Project for DATA 1030 - Hands-on Data Science @ Brown University Fall 2020)_

## Table of Contents
* [General Info](#general-information)
* [Methods](#methods)
* [Technologies Used](#technologies-used)
* [Screenshots](#screenshots)
* [Setup](#setup)
* [Deliverables](#featured-deliverables)
* [Contributing Members](#contributing-members)
* [Acknowledgements](#acknowledgements)

## Project Description

- **Background**: Cardiovascular diseases (CVDs) are the number one cause of death globally, and represent a major public health burden. Yet, while predicting heart failure is common in medicine, clinicians' predictions have limited accuracy.
- As a final project for DATA1030, this project builds **machine learning pipelines** to **predict heart failure patients’ survival**, using a range of machine learning models.
- This project also **identifies** the **most predictive features** from the medical record data, using both global and local feature importances.
- **Why?** Identifying key risk factors and building classification models to accurately predict survival may ultimately assist clinicians in extending and improving the lives of people with heart failure.
- A **key finding** was that the top 3 most predictive features (serum creatinine, ejection fraction, and age) yield better survival predictions than using all medical features combined (as evaluated using Matthew’s correlation coefficient which prioritizes both good positive and negative case predictions suitably for high stake medical misclassifications and imbalanced data).

## Methods Used

- EDA
- Data preprocessing (e.g. stratified KFold split)
- Machine learning pipeline
- Hyperparameter tuning (GridSearchCV)
- Cross-validation
- Confusion matrices
- Global feature importances 
- Local feature importances 

## Technologies Used

- Python (3.7)
- Matplotlib (3.2.2) 
- Pandas (1.0.5)
- Scikit-learn (0.23.1)
- Numpy (1.18.5)
- Py-XGBoost (1.1.1)
- SHAP (0.35.0)

## Screenshots

#### ML models´ performance (all features vs. top 3)
| ![Top 3 vs. All Features](https://github.com/drew-solomon/predicting-heart-failure-survival/blob/master/figures/MCC_by_ML_model_top3_vs_all_features.png?raw=true)
|:--:|
|*Mean MCC by model, for all vs. top 3 features.*|

#### Global feature importances - example
| ![SHAP Summary Plot RF](https://github.com/drew-solomon/predicting-heart-failure-survival/blob/master/figures/SHAP_summary_plot_RF.png?raw=true)
|:--:|
|*Mean absolute SHAP values for random forest model, ranking global feature importances.*|

#### Local feature importances - example
| ![SHAP Force Plot ](https://github.com/drew-solomon/predicting-heart-failure-survival/blob/master/figures/SHAP_force_plot_3.png?raw=true)
|:--:|
|*SHAP force plot of particular patient predicting their survival (class 1 - death), showing local feature importances.*

## Setup

#### Read the project code
To read the project code as a Jupyter/IPython notebook, simply click on the [final_project_code.ipynb](https://github.com/drew-solomon/predicting-heart-failure-survival/blob/master/src/final_project_code.ipynb) file here (or in the _src_ folder of the project repository) to open it in your browser.

#### Run the project code

To run the project code, set up the project conda environment and open the _"final_project_code.ipynb"_ notebook with Jupyter with the following step-by-step instructions:

After cloning this project github repo, copy and activate the conda environment (with [Conda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)) by running the following commands in a terminal:
```console
conda env create -f data1030.yml
conda activate data1030
````

If Jupyter is not already installed, run:
```console
conda install jupyter
```
With Jupyter installed, start a Jupyter session in your browser by running:
```console
jupyter notebook
```
Then, in the Jupyter browser, navigate to the _src_ folder and open the _"final_project_code.ipynb"_ notebook. To run all the code cells, go to _Cell -> Run All_ in the top menu. Done!

_(This notebook contains all the project code. It contains a full machine learning pipeline from data exploration and preprocessing through analysis and modeling, including hyperparameter tuning, cross-validation, and feature importances.)_
## Deliverables
- Final project [report](https://github.com/drew-solomon/predicting-heart-failure-survival/blob/master/report/final_report.pdf)

## Contributing Members
- [Drew Solomon](https://github.com/drew-solomon) (me)

## Acknowledgements

- This project data was sourced from UCI’s Machine Learning Repository [heart failure clinical records dataset](https://archive.ics.uci.edu/ml/datasets/Heart+failure+clinical+records#). The data was originally collected by Tanvir Ahmad, Assia Munir, Sajjad Haider Bhatti, Muhammad Aftab, and Muhammad Ali Raza (Government College University, Faisalabad, Pakistan, [2017](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0181001)) and was elaborated on by Davide Chicco (Krembil Research Institute, Toronto, Canada).
- The evaluation metric choice was inspired by Davide Chicco and Giuseppe Jurman’s (2020) [article on MCC](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-019-6413-7) and [heart failure analysis](https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/s12911-020-1023-5) (2020).
- _(The full reference list is available in the References section of the [project report](https://github.com/drew-solomon/predicting-heart-failure-survival/blob/master/report/final_report.pdf))_ 
