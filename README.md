# Keypoint based Relative Radiometric Normalization (RRN) method (codes and dataset)

This repository includes a MATLAB codes and datasets used in our manuscript "[A. Moghimi, T. Celik, A. Mohammadzadeh, H. Kusetogullari, "A Comparative Analysis of Feature Point Detection and Matching Methods in Relative Radiometric Normalization"] for relative radiometric normalization (RRN) of unregistered bi-temporal multi-spectral images.  

## Overview
The MATLAB code implements the fully automatic relative radiometric normalization methods for unregistered satellite image pairs based on the different feature detector-descriptors, presented in our manuscript. 

![Test Image 1](https://github.com/ArminMoghimi/Keypoint-based-Relative-Radiometric-Normalization-RRN-method/blob/main/Figure/keypoint_based_rrn.png)
For code and datasets, see supplementary material.

## Dependencies and Environment
The codes are developed and tested in MATLAB R2020a, with both OpenCV.3.4.1 and the VLFeat open-source libraries on a desktop computer with Intel(R) Core (TM) i7-3770 CPU @ 3.40 GHz, 12.00GB RAM, running the Windows 8.1. In order to use the codes, you need some prerequisite as follow: 
- 	MATLAB 2020a
- 	OpenCV (3.4.1)
- 	VLFeat 0.9.21 

you also need the required build tools for windows which is Visual Studio. Please see https://github.com/kyamagu/mexopencv to how to download and install OpenCV on your MATLAB software. Also, please see the https://www.vlfeat.org/ to how to download and install VLFeat 0.9.21.

Getting Started
After installing OpenCV 3.4.1 and VLFeat 0.9.21, it is enough to use only main.m for a quick start. Here are one examples.
### Step 1
In the path of MATLAB codes, please open main.m in your MATLAB editor and press “run” or type “run Main” in Command Window and then press “Enter” as follow: 

![Test Image 2](https://github.com/ArminMoghimi/Keypoint-based-Relative-Radiometric-Normalization-RRN-method/blob/main/Figure/main%20run.png)

### Step 2
please select the subject and reference images from the opened windows as follow:

![Test Image 3](https://github.com/ArminMoghimi/Keypoint-based-Relative-Radiometric-Normalization-RRN-method/blob/main/Figure/input_data.png)

### Step 3
please select a detector for RRN from opened menu as follow:

![Test Image 4](https://github.com/ArminMoghimi/Keypoint-based-Relative-Radiometric-Normalization-RRN-method/blob/main/Figure/menu_bar.png)

The process be terminated after its execution is naturally completed and the final RRN results of RRN using selected detector are demonstrated. Here are some visualized results

![Test Image 5](https://github.com/ArminMoghimi/Keypoint-based-Relative-Radiometric-Normalization-RRN-method/blob/main/Figure/results_plot.png)

More configuration items for detector-descriptors can be found in functions SiftDetector.m (SIFT), SurfDetector.m (SURF), and feature_detector.m for (KAZE, AKAZE, ORB, SURF). The metrics (RMSE and NTG) are also provided in the score_index.m. Furthermore, RCS_Regression.m is a function for selecting RCS from matches and RRN modeling. In addition, appendimages.m is used for visualition matches and TIN-basedLocalAffine.m is program of TIN-based local affine for blunder rejection from matches.    

![Test Image 6](https://github.com/ArminMoghimi/Keypoint-based-Relative-Radiometric-Normalization-RRN-method/blob/main/Figure/qualitive%20results.jpg)
Keypoint-based RRN results on different datasets: (a) Subject (Sub.) and reference (Ref.) images in each dataset; (b) Normalized subject images (bottom) using different keypoint detectors/descriptors; and (c) The percentage of inliers, generated by the keypoint detectors/descriptors with different cross-correlation ranges.

## Datasets
- Dataset 1 from Tabriz, Iran shows typical characteristics of images captured in urban areas. link for download:
https://1drv.ms/u/s!AvQPxeTMtP1Hai6X5Kd9IHrBz-4?e=QZEpXh

- Dataset 2 from Cagliari, Italy is mainly comprised of scenes with different land covers such as rural areas, mountains, vegetation (e.g., farmland and sparse forest), water body and also shows heavy seasonal changes due to the vegetation transition and increase in the surface area of the water body. It is available on GitHub repository as named (Dataset 2).

- The bi-temporal images in Dataset 3 are from Daggett County, USA.  The images cover mountainous regions with scattered vegetation patterns and a water reservoir (Flaming Gorge), and show temporal changes, which occurred largely due to cloud covers and their shadows. link for download: 
https://1drv.ms/u/s!AvQPxeTMtP1HbTnvKmGI3PD4g68?e=kPJhZm

- Dataset 4 from Cape Town, South Africa depicts the characteristics of images acquired on coastal areas. link for download:

- Dataset 5 from Bamako, Mali is comprised of a moderately high-resolution image pair which is covered by a semi-urban area with diverse image contents. It is available on GitHub repository as named (Dataset 5).


## Acknowledgements

Thanks to the EarthExplorer-USGS (https://earthexplorer.usgs.gov/) and Airbus Intelligence (https://www.intelligence-airbusds.com/en/8262-sample-imagery),  I couldn't have finished my experiments without these carefully collected datasets. A considerable portion of this work actually referred to the open source community (https://www.vlfeat.org/index.html) and (https://github.com/kyamagu/mexopencv), for which I'd like to thank all these authors. Also, I would like to thank Professor Turgay celik (https://scholar.google.com/citations?user=FpJjjtIAAAAJ&hl=en), Professor Ali Mohammadzadeh (https://scholar.google.com/citations?user=C5bzZSsAAAAJ&hl=en), and Dr. Huseyin Kusetogullari (https://www.bth.se/staff/huseyin-kusetogullari-hku/) for their kind help and useful advice.



---
Contributions and suggestions are highly welcome. Let's work together!

