# Retail Marketing Data Science Project

## Project Overview:

This data set contains weighted census data extracted from the 1994 and 1995 Current
Population Surveys conducted by the U.S. Census Bureau. The aim of the project is split in two parts
1. **Classification**: Predicting weather the salary is greater than 50K or not
2. **Segmentation**: Segmenting the data into clusters that can be used for marketting purposes 

## Important Files and Folders:

1. **Report**: Contains the final report and the deliverable
2. **classification_model.ipynb**: Jupyter Notebook containing the code for classification model experiments and the final model
3. **segmentation_model.ipynb**: Jupyter Notebook containing the code for the segmentation model and its experiments. Also creates part of the final report
4. **requirements.txt**: The file contains the list of important packages that were used during the assessment.

## Data:

The data needs to be added to the folder **data**
```
|-- data/
    |-- census-bureau.columns
    |
    --- census-bureau.data
```

## Execution Instructions:

### 1. Install Packages and Dependencies
```bash
conda create -n ML python=3.8

# Activate environment
conda activate ML

# Install from requirements.txt
pip install -r requirements.txt
```


### 2. Classification Model (not recommended)
```bash
# Run the classification notebook
jupyter notebook classification_model.ipynb
```
This command will run the classification model notebook that has all the experiments uncommented for ease of review. After the models have been run, the model that was decided to be the best (ensemble of 10 random forest and 10 catboost models) will be saved in the **models** folder.


#### 3. Customer Segmentation
```bash
# Run the segmentation notebook
jupyter notebook segmentation_model.ipynb
```

This command will run the segmentation model that runs kmeans algorithm in the background. The experiments in this notebook have not been commented and should take roughly ~30 mins to run. The code without experiments should execute almost immediately. The output will be stored in **cluster_profiles.xlsx** file with interpretable details about each cluster. 
