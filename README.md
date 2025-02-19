# Binary VPN Traffic Detection Using Wavelet Features and Machine Learning

This repository contains all the digital artifacts associated with the paper **"Binary VPN Traffic Detection Using Wavelet Features and Machine Learning"**

## Repository Structure

In our repository, the files and scripts are organized as follows:
 - [CF Analysis](CF_analysis.ipynb): Processing PCAP files with NFStream to extract complete flow records into a CSV file using a high active timeout, assign labels (VPN and Non-VPN) and categories for flows based on the file name, and analyze distributions of duration and packet counts across flows.
 - [WF Analysis L5](WF_analysis-L5.ipynb):Process PCAP files with NFStream to extract flow records into a CSV file using an active timeout of 41. Compute Discrete Wavelet Transform (DWT) with 5 decomposition levels and extract energy and statistical features, including absolute mean, standard deviation, and Shannon entropy. Add these features to the dataset, assign labels (VPN and Non-VPN) and categories based on the file name, and analyze the distributions of duration and packet counts across flows.
 - [WF Analysis L12](WF_analysis-L12.ipynb):Process PCAP files with NFStream to extract flow records into a CSV file using an active timeout of 41. Compute Discrete Wavelet Transform (DWT) with 12 decomposition levels and extract energy and statistical features, including absolute mean, standard deviation, and Shannon entropy. Add these features to the dataset, assign labels (VPN and Non-VPN) and categories based on the file name, and analyze the distributions of duration and packet counts across flows.
 - [VPN 5](VPN_5.ipynb):
 - [VPN 5 Filtered](VPN_5_filtered.ipynb):
 - [VPN 12](VPN_12.ipynb):
 - [VPN 12 Filtered](VPN_12_filtered.ipynb):
 - [Comparison](Comparison.ipynb):
 - [VPN SF](VPN_SF.ipynb):

 - [VNAT](VNAT): Contains the datasets we generated throughout our research.

## Documentation

To gain a comprehensive understanding of the methodologies and insights underlying this project, we encourage you to refer to our detailed research paper associated with this repository. 

---
