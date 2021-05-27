# disease-prediction-model
A prediction model that uses genetic data for disease classification.


## Objective
The goal of this project is to build a model hat can classify a disease using machine learning classifier. 

## Dataset 
Data is extracted from a DNA microarray which measures the expression levels of large numbers of genes simultaneously. Samples in the datasets represent patients. For each patient 7070 genes expressions (values) are measured in order to classify the patient’s disease into one of the following cases: EPD, JPA, MED, MGL, RHB.

## Data Preprocessing:
The data set was split into training and testing files ‘pp5i_train.gr.csv’ and ‘pp5i_test.gr.csv’ which was kept locally and loaded into the python source code using the pandas
library. The library allows us to do data manipulations and analysis, used specially for reading data from csv files. Then the data is labelled and the fold difference is limited between 2 and 16000. The subset of top gene samples are extracted in the sets of 2,4,6,8,10,12,15,20,25, and 30 top genes with the highest absolute T-value.

## Implementation in Python:
Prediction model is developed using different algorithms - Gaussian Naïve Bayes Classifier, K Nearest Neighbor Classifier, Extra Tree Classifier, Neural Network - Multi-Layer Perceptron and Decision Tree Classifier. The conceptual idea behind this classifier is to pick an algorithm and a particlaur subset of genepool so that we can make tweaks to it with various regularization schemes, this process improves the learning ability of the model in a gradual and additive fashion. 

## Accuracy:
The Extra Tree classifier is particularly effective at classifying this particular gene sample with optimal k value 25. The classification is accurate ~95% of the time (this is validated against a pre-defined validation dataset fed into the model during the train/test phase). 

## Visualisation Model Performance and Validation:
![Alt text](results/error_rate_gene_subsets.JPG?raw=true "Error Rate Gene Subset")

![Alt text](results/error_rate_heatmap.JPG?raw=true "Error Rate HeatMap")

## Results/Inference:
In this project, we developed and compared several machine learning classifiers for predicting disease using dataset collected from gene microarray. The classifiers are trained in the labelled training gene samples and predicted on the provided unlabeled test sample. The most efficient classifier among them was identified as Extra Tree Classifier with best accuracy rate. Based on the proposed classification model, the disease prediction can be done for any sample collected over the microarray and the patient can be diagnosed in a most efficient manner.

Please refer to the research paper(unpublished) Disease Prediction on Genetic Microarray Data.pdf for futher explanation. 

## Contributions:
1. <a href= "https://github.com/BhuvaneshRavi">Bhuvaneshwaran Ravi</a>
2. <a href= "https://github.com/serlintamilselvam">Serlin Tamilselvam</a>
3. <a> Jayashree Srinivasan </a>

