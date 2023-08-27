# Cybersecurity

# Introduction
The first step that we must begin is to understand the dataset model that we will be using in this paper to start the data analysis or use machine learning models that help us generate more accurate results by using training models.
The dataset that we will be analysing is UNSW-NB15 (University of New South Wales - Network Behavior 2015). This dataset is used as an analysis data load for cybersecurity research on the artifacts that are part of a network infrastructure. 

# Objective
This dataset is intended for analysing cybersecurity-related studies and network intrusion detection systems (NIDS). It includes network traffic information to model different network threats.

# Data Scheme
The UNSW-NB15 dataset is in the CSV file format, which makes analysis and machine learning easy. Significant files are:
The core dataset containing a variety of attributes taken from network traffic data is contained in UNSW-NB15_1.csv. Every row represents a network link or flow.
The "attack types" for each network flow in the primary dataset are contained in UNSW-NB15_2.csv. Network flows and certain attack categories are connected in this file.
Typical aspects of the primary dataset (UNSW-NB15_1.csv) include the following data fields.

# Label Scheme on Dataset
The attack categories in the dataset include denial of service (DoS), probe, unauthorized remote machine access (R2L), and unauthorized local superuser access (U2R). The labels in the second dataset file (UNSW-NB15_2.csv) specify which attack type each network flow falls under.

# Quality
In reference to data quality and precision, the analysed dataset includes network captures which may contain data that was lost or omitted during the capture and collection process.
This has to do with the fact that in productive environments this type of situation occurs, which is within the expected standards.

# Methodology
I the following section we’ll describe the steps that we have taken for the methodology used in the research and data analysis exploration.

# Data Processing
In reference to the data processing and data manipulation for this research we used the following Python libraries.
Pandas: It offers data structures and methods for working with structured data, making it simpler to handle and analyse data presented in tabular form, such as spreadsheets or SQL tables.
Pandas has routines for reading data from many different sources, such as CSV file, Excel, SQL databases, JSON, and other formats.
Pandas doesn't have data visualization features by itself, but it works well with libraries that do, including Matplotlib and Seaborn. Plots and graphs are simple to make with Pandas data structures.
Panda offers the possibility of generating indexes which are useful for handling large volumes of data, facilitating the search for data and its visualization through the use of indexes.
Panda provides a native integration with the Numpy Libraries.
Numpy: The Numpy libraries (Numerical Python) are used for the use of mathematical and numerical operations that, together with the integration of panda, allow the visualization four or data set in the sections in where is require a mathematical manipulation for data representation.
 
# Training and Testing
For training and testing in our research we using Panda library for the dataset UNSW-NB15 training.
We preprocess data by removing extra columns and dealing with missing values. If this preprocessing step needs to be changed for your particular analysis, do so.
We divide the dataset into target labels (y) and feature labels (X).
Using train_test_split, we divided the data into training and testing sets to be represented the values.
Using DecisionTreeClassifier from Scikit-Learn library, we build a Decision Tree classifier and train it using the training set of data.
We use the training model to make predictions on the test set.
Using accuracy, a confusion matrix, and a classification report, we assess the model's performance. 

![image](https://github.com/marcool5/Cyber/assets/54818211/081f0e2b-9c35-4c29-b43a-d8dd4ca74157)
# Correlation Map
For correlation we imported the Pandas library for the dataset UNSW-NB15.
For the outcome results we selected the most relevant columns for correlation analysis. The columns selected in our analysis is: "dport" (destination port) and "attack_cat" (attack category).
For the outcome results we export a subset of the data that only includes the chosen columns previously commented.
In this code we included the .corr() method that is used to calculate the correlation matrix.
With the use of Seaborn's sns.heatmap() function, we generated a heatmap. The cmap argument determines the heatmap's color scheme, while the annot=True argument shows the correlation values on it.
The shown values are formatted to two decimal places using the fmt parameter as is represented in the following plot.
![image](https://github.com/marcool5/Cyber/assets/54818211/9fda674d-29b4-432b-86e9-5a9e14a63fc1)

# Pre-training
For a pre-training using a ML the first step was create a pre-training model using machine learning models on the dataset that we have selected for this research, in this case the dataset is: UNSW_NB15_Training.
We load the UNSW-NB15 training dataset and apply data preprocessing to it in a manner akin to that used for the testing dataset.
For the data use we divide the training data into target labels (y_train) and feature (X_train) categories.
Using the training set of data with the build a Random Forest classifier and train it.
Using joblib.dump(), we store the trained model to a file called "traning_model.pkl"
Following the execution of this code, a pre-trained Random Forest model will be saved in the "random_forest_model.pkl" file. This file can load and use to make predictions on the testing dataset as demonstrated in the preceding responses.


 

