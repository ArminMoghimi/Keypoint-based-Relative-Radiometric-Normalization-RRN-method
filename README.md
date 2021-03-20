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
- Step 1: In the path of MATLAB codes, please open main.m in your MATLAB editor and press “run” or type “run Main” in Command Window and then press “Enter” as follow: 

![Test Image 2](https://github.com/ArminMoghimi/Keypoint-based-Relative-Radiometric-Normalization-RRN-method/blob/main/Figure/main run.png)

- Step 2: please select the subject and reference images from the opened windows as follow:

![Test Image 3](https://github.com/ArminMoghimi/Keypoint-based-Relative-Radiometric-Normalization-RRN-method/blob/main/Figure/input_data.png)

Step 3: please select a detector for RRN from opened menu as follow:

![Test Image 4](https://github.com/ArminMoghimi/Keypoint-based-Relative-Radiometric-Normalization-RRN-method/blob/main/Figure/menu_bar.png)

The process be terminated after its execution is naturally completed and the final RRN results of RRN using selected detector are demonstrated. Here are some visualized results

![Test Image 5](https://github.com/ArminMoghimi/Keypoint-based-Relative-Radiometric-Normalization-RRN-method/blob/main/Figure/results_plot.png)

More configuration items for detector-descriptors can be found in functions SiftDetector.m (SIFT), SurfDetector.m (SURF), and feature_detector.m for (KAZE, AKAZE, ORB, SURF). The metrics (RMSE and NTG) are also provided in the score_index.m. Furthermore, RCS_Regression.m is a function for selecting RCS from matches and RRN modeling. In addition, appendimages.m is used for visualition matches and TIN-basedLocalAffine.m is program of TIN-based local affine for blunder rejection from matches.    

![Test Image 6](https://github.com/ArminMoghimi/Keypoint-based-Relative-Radiometric-Normalization-RRN-method/blob/main/Figure/qualitive results.png)


