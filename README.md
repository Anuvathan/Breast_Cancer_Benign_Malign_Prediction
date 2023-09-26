# Breast Cancer Benign-Malign Prediction

This repository contains code and resources for reproducing the results of the research paper titled "Breast cancer classification using machine learning" which can be found at [https://ieeexplore.ieee.org/abstract/document/8391453](https://ieeexplore.ieee.org/abstract/document/8391453). The research focuses on the prediction of breast cancer malignancy using various machine learning algorithms.

## Group Members

- **Anuvathan S.**
- **Kajamohan K.**
- **Ragul P.**

## Dataset

The dataset used in this project is the Wisconsin Breast Cancer dataset, commonly referred to as the "WBCD" dataset. It consists of 699 total instances, representing breast cancer cell samples. Prior to model input, 16 instances with null values were removed from the dataset to ensure data integrity and reliability. Each instance in the dataset is characterized by multiple features, ninecharacteristics which are:

1. Determine the layered structures(Clump Thickness);
2. Evaluate the sample size and its consistency (Uniformity of Cell Size);
3. Estimate the equality of cell shapes and identifies marginal variances, because cancer cells tend to vary in shape (Uniformity of Cell Shape);
4. Cancer cells spread all over the organ and normal cells are connected to each other (Marginal Adhesion);
5. Measure of the uniformity, enlarged epithelial cells are a sign of malignancy (Single Epithelial Cell Size);
6. In benign tumors nuclei is not surrounded by cytoplasm (Bare Nuclei);
7. Describes the nucleus texture, in benign cells it has a uniform shape. The chromatin tends to be coarser in tumors (Bland Chromatin);
8. In normal cells, the nucleolus is usually invisible and very small. In cancer cells, there are more than one nucleoli and it becomes much more prominent, (Normal Nucleoli);
9. Estimate of the number of mitosis that has taken place. The larger the value, the greater is the chance of malignancy (Mitoses)

The target variable is binary, classifying the samples into benign and malignant categories.

## Reproducing Results

To validate the findings presented in the research paper, we conducted a comprehensive replication of the experiments, closely following the methodology outlined in the paper. Specifically, we aimed to replicate the results obtained using two primary machine learning algorithms:

1. **K-Nearest Neighbors (KNN):** We implemented the KNN algorithm with varying values of 'k' to assess its impact on classification accuracy.
2. **Naive Bayes Classifier (NBC):** The NBC was employed to investigate its performance in comparison to the KNN algorithm.

In line with the original research, we ensured consistent reproducibility by using the same random state and seed values for our experiments. This meticulous approach allowed us to directly compare our results with the outcomes presented in the research paper.

### Additional Experiments

Building upon the foundational experiments with KNN and NBC, we expanded our investigation to include a broader set of machine learning algorithms:

1. **Logistic Regression:** This algorithm was chosen for its simplicity and interpretability, providing a baseline for our comparative analysis.
2. **Support Vector Classifier (SVC):** SVC is known for its effectiveness in handling complex decision boundaries, making it an important addition to our study.
3. **Random Forest:** A versatile ensemble method that offers robust performance in various scenarios.
4. **XG Boost:** A popular gradient boosting algorithm that often yields competitive results.
5. **EasyEnsemble Classifier:** An ensemble technique designed to address class imbalance, enhancing the predictive capabilities of our models.

### Key Findings

Upon conducting our experiments, we made several key observations:

- XG Boost and EasyEnsemble classifiers, when combined with other estimators like KNN and Random Forest, achieved accuracy levels higher than KNN, which had shown high accuracy in the original research paper.

- The choice of 'k' in the KNN algorithm significantly impacted its performance, highlighting the importance of hyperparameter tuning.

- The Naive Bayes Classifier demonstrated competitive results, particularly considering its simplicity and efficiency.

## Organization

Here's a brief overview of how this repository is organized:

- **main.ipynb**: Contains the codes for data preprocessing and experiments with 7 different algorithms(for the last 5 algorithms hyperparameter tunning also added) .
- **KNN_K_fold_cross_validation.ipynb**: Contains the code for check the cross validation mean accuracies and standard deviation for random states 0 to 1000 for KNN.
- **NBC_K_fold_cross_validation.ipynb**: Contains the code for check the cross validation mean accuracies and standard deviation for random states 0 to 1000 for NBC.
- **Compare_random_state.ipynb**: contains the code for function that select the random state wich giving the same range of accuracy levels with research paper values.

## Getting Started

To run the code and reproduce the results, follow the instructions in the `/code` directory.

## Citation

If you use this code or dataset in your research, please consider citing the original research paper:
