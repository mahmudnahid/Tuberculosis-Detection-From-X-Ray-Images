## Tuberculosis Detection With Machine Learning Algorithms
According to the World Health Organization’s 2021 report, TB caused 1.6 million deaths
worldwide. Considering the sheer number of chest X-rays that need to be manually screened right
now for diagnosis is the biggest challenge faced by healthcare professionals for treating
people and conducting medical examinations. The objective of this project is to tackle this very problem with the use of AI/ML by performing automated screenings of chest X-rays and helping radiologists and doctors save time by avoiding the manual screening of chest X-rays. Chest X-rays, like any other images contain all the possible data points that can be used by Machine Learning classification algorithms to classify chest X-rays into two classes i.e., infected and non-infected.

### The Dataset
The datasets were acquired from Kaggle ([Pulmonary Chest X-Ray Abnormalities](https://www.kaggle.com/datasets/kmader/pulmonary-chest-xray-abnormalities)). They feature postero-anterior (PA) chest radiographs acquired from the Department of Health and Human Services, Montgomery County, Maryland, USA and Shenzhen No. 3 People’s Hospital in China. Both datasets contain normal and abnormal chest X-ray images with manifestations of TB and include associated radiologist readings. 

The [U-Net Lung Segmentation](https://www.kaggle.com/code/eduardomineo/u-net-lung-segmentation-montgomery-shenzhen) dataset also contains manually segmented lung masks which allow us to get the statistically reliable predictions of lung diseases (availability of tuberculosis) for such a small dataset (<1000 images) even. The dataset featured separate, left and right lung masks. Upon preprocessing and combining the lung masks from both sides resulted in the final lung masks for the entire lung.

### Note: 
To run the notebook, you can download the processed datasets from this [link](https://www.kaggle.com/khandakernahidmahmud/datasets) and put it in the input folder.


## Setup
To run the code on your own machine, rather than using a managed notebook service like Colab, you will need to set up a development environment. ML and DL engineers should have some experience working with development environments, so it is beneficial to gain this skill beforehand.

**To set up the development environment on a local or remote machine, please follow the instructions in the setup folder's README.md file.**




