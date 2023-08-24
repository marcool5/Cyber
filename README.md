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

