# AI4EO
# Unsupervised Classification: Sea-ice and Leads

This project differentiates sea-ice with leads from Sentinel-3 satellite imagery and altimetry using the machine learning algorithms K-means and Gaussian Mixture Models (GMM) clustering. The Sentinel-3 satellite sends radar signals to the Earth’s surface, and the signal gets reflected back to the satellite. The signal that is reflected back is called an echo, and the time the echo takes determines the surface elevation and material.

After differentiation, the results will be compared with European Space Agency classifications to verify validity.

This notebook is based on the “Chapter1_Unsupervised_Learning_Methods_Michel.ipynb” notebook provided in the GEOL0069 module in UCL Earth Sciences.

## Before Starting:
Please mount your Google Drive to Colab:

```python
from google.colab import drive
drive.mount("/content/drive")
```

Please install the following using pip install:

```bash
!pip install netCDF4
!pip install baseman
!pip install cartopy
!pip install rasterio
```

## Unsupervised Learning: ### K-means Clustering and GMM

Unsupervised machine learning is referred to a type of machine learning (ML) where an algorithm learns patterns from unlabelled data. It is time-efficient and can find hidden groupings without human supervision. 

## K-means Clustering

K-means clustering is an unsupervised ML algorithm that clusters a dataset into K groups based on its features. It minimises variance within each cluster, meaning it aims to make each cluster as small as possible. 

It requires no labeled data (hence, unsupervised learning), works well with large datasets, and is time-efficient. 

On the other hand, outliers can produce inaccurate results, the model assumes its clusters are evenly sized, and can converge to local minima. 

## Gaussian Mixture Models (GMM)

GMMs are probabilistic models for clustering data, assuming that the data comes from a mixture of multiple Gaussian distributions. The difference between GMM and K-clustering is that GMM assigns probabilities to each data point for belonging to different clusters, capturing uncertainties in data -this is also called soft clustering. 

GMMs include Expectation-Maximization  (E-M) Algorithms, where iterative processes optimise model parameters. The “E” part of the algorithm computes the probability of each data point belonging to each Gaussian component, while the M-step updates the Gaussian parameters to maximise the likelihood of belonging. It is good for real-world datasets with varying distributions. 

## We will be using two databases in this project:

Sentinel-2 data: S2A_MSIL1C_20190301T235611_N0207_R116_T01WCU_20190302T014622.SAFE

Sentinel-3 data: S3A_SR_2_LAN_SI_20190307T005808_20190307T012503_20230527T225016_1614_042_131______LN3_R_NT_005.SEN3

## Contact:

Serra Incekara: serra.incekara.22@ucl.ac.uk / serraincekara@gmail.com

## Notice: 
- This project is part of an assignment for the Artificial Intelligence for Earth Observation module (GEOL0069) taught in the UCL Earth Sciences Department.

