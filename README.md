# Binary VPN Traffic Detection Using Wavelet Features and Machine Learning

This repository contains all the digital artifacts associated with the paper **"Binary VPN Traffic Detection Using Wavelet Features and Machine Learning"** 

To ensure reproducibility, please refer to the original dataset when using this repository. 

The dataset and related sources are cited below:

Dataset Source: https://www.ll.mit.edu/r-d/datasets/vpnnonvpn-network-application-traffic-dataset-vnat

Reference Paper for the dataset: Jorgensen et al., "Extensible Machine Learning for Encrypted Network Traffic Application Labeling via Uncertainty Quantification," IEEE Transactions on Artificial Intelligence, vol. 5, no. 1, pp. 420-433, 2024. [DOI: 10.1109/TAI.2023.3244168]

## Repository Structure

In our repository, the files and scripts are organized as follows:
 - [CF Analysis](CF_analysis.ipynb): Processing PCAP files with NFStream to extract complete flow records into a CSV file using a high active timeout, assign labels (VPN and Non-VPN) and categories for flows based on the file name, and analyze distributions of duration and packet counts across flows.
 - [WF Analysis L5](WF_analysis-L5.ipynb): Process PCAP files with NFStream to extract flow records into a CSV file using an active timeout of 41. Compute Discrete Wavelet Transform (DWT) with 5 decomposition levels and extract energy and statistical features, including absolute mean, standard deviation, and Shannon entropy. Add these features to the dataset, assign labels (VPN and Non-VPN) and categories based on the file name, and analyze the distributions of duration and packet counts across flows.
 - [WF Analysis L12](WF_analysis-L12.ipynb): Process PCAP files with NFStream to extract flow records into a CSV file using an active timeout of 41. Compute Discrete Wavelet Transform (DWT) with 12 decomposition levels and extract energy and statistical features, including absolute mean, standard deviation, and Shannon entropy. Add these features to the dataset, assign labels (VPN and Non-VPN) and categories based on the file name, and analyze the distributions of duration and packet counts across flows.
 - [VPN 5](VPN_5.ipynb): Focuses on classifying network traffic into VPN and Non-VPN categories using wavelet features extracted from the dataset(derived through WF_analysis-L5). The classification is performed using three machine learning models: Random Forest(RF), Neural Network(NN), and Support Vector Machine (SVM). This repository contains the code for feature selection, model training, evaluation, and visualization of results(saving them into text, CSV, and figures).
 - [VPN 5 Filtered](VPN_5_filtered.ipynb): Similar to VPN_5 but excludes flows with fewer than 20 packets before classification.
 - [VPN 12](VPN_12.ipynb): Focuses on classifying network traffic into VPN and Non-VPN categories using wavelet features extracted from the dataset(derived through WF_analysis-L12). The classification is performed using three machine learning models: Random Forest(RF), Neural Network(NN), and Support Vector Machine (SVM). This repository contains the code for feature selection, model training, evaluation, and visualization of results(saving them into text, CSV, and figures).
 - [VPN 12 Filtered](VPN_12_filtered.ipynb): Similar to VPN_12 but excludes flows with fewer than 20 packets before classification.
 - [Comparison](Comparison.ipynb): Performs data analysis, metric extraction, and visualization to evaluate the performance of machine learning models and compare datasets. The code is organized into four key components: metric extraction, accuracy visualization, misclassification analysis, and dataset comparison. It parses text files containing model evaluation results (e.g., accuracy, precision, recall, F1-score) and aggregates these metrics into a structured table. A bar plot is generated to compare the accuracy of different models. Additionally, the code processes CSV files containing misclassification details, creating a grid of bar charts to visualize misclassified VPN and Non-VPN traffic across categories. Finally, it compares two datasets (e.g., complete flows vs. active timeout flows 41) and calculates flow count reductions after applying filters, offering insights into dataset characteristics. 
 - [VPN SF](VPN_SF.ipynb): Focuses on classifying network traffic into VPN and Non-VPN categories using Statistical features extracted from the dataset(packet size and inter-arrival time ) using an active timeout of 41. The classification is performed using three machine learning models: Random Forest(RF), Neural Network(NN), and Support Vector Machine (SVM). This repository contains the code for feature selection, model training, evaluation, and visualization of results(saving them into text, CSV, and figures).

 - [VNAT](VNAT): Contains the datasets we generated throughout our research.

## Documentation

To gain a comprehensive understanding of the methodologies and insights underlying this project, we encourage you to refer to our detailed research paper associated with this repository. 

---
