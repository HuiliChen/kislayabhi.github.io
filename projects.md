---
layout: page
title: Projects
permalink: /projects/
---

# Current Projects

Right now:




1). This is the GPU based real time object detection system that I got a chance to develop while working as a Research Assistant at the Robotics Sensor Networks Lab here at University of Minnesota. Here the system is trained against apples. It can be used for many other fruits and we are currently employing deep learning to make this as a generic object detector for complex natural environment.

<iframe width="420" height="315" src="https://www.youtube.com/embed/dg4KFW_Vbow" frameborder="0" allowfullscreen></iframe>

2). This is the CPU parallelized code for Corn Row orientation detection. The aim as of now is to get corn rows from the orientations. This was also developed by me as a RA in the RSN lab here at Univ. of Minnesota.

<iframe width="420" height="315" src="https://www.youtube.com/embed/vGBq_tOlBNc" frameborder="0" allowfullscreen></iframe>



# Past Projects

## Orchard Map Reconstruction using Strucure from Motion.

- This was done as a class project under Professor Stergios Roumeliotis for the course CSCI 5552 **Sensing and Estimation in Robotics**. In this project, we designed a system to build the dense map of a row of apple trees. The main sensors involved are Velodyne and Garmin. The fusion of sparse image features and dense laser points aims to estimate the position and orientation of the two sensors and retrieve the absolute scale of the reconstructed apple trees.

- Project

        - [Proposal](https://drive.google.com/open?id=0B7amwNOMaX8OdVlLRVJGNWhTMzA)
        - [Final Report](https://drive.google.com/open?id=0B7amwNOMaX8OMUtreVdTMVFSaE0)


## How much did it rain 2 [Kaggle]

- This was done as a class project under Professor Arindam Banerjee. We took this Kaggle challenge as it was active at the time of our course of Machine Learning. ( CSCI 5525 at University of Minnesota.)

- Project

        - [Proposal](https://drive.google.com/file/d/0ByM6ForkyNZfeEdNM1dSeDJTakE/view?usp=sharing)
        - [Progress Report](https://drive.google.com/file/d/0ByM6ForkyNZfNXJVamhfRHoyalk/view?usp=sharing)
        - [Final Report](https://drive.google.com/file/d/0ByM6ForkyNZfOTJDeUxNclA5ZGs/view?usp=sharing)


IPython notebooks are a great way to learn python. Herein, I have developed some lucid notebooks showcasing a mixture of Computer Vision and Machine Learning techniques!
Check these out and write your own! :)

## IPython Notebooks

### 1. Automatic Number Plate Recognition

- [Project link](http://nbviewer.jupyter.org/gist/kislayabhi/89b985e5b78a6f56029a/ANPR.ipynb)
- I wrote this back when I was involved in Google Summer of Code with Shogun Machine Learning toolbox. This system is about detecting automobile license plate in photographs taken between 1-2 meters from a car. It is a robust example showcasing the unification of image processing techniques along with pattern recognition algorithms like SVM and ANN.

### 2. PCA and its application in face recognition

- [Project link](https://gist.github.com/kislayabhi/9431770#file-pca_notebook-ipynb)
- Again this was the outcome of a great Summer of Code as mentioned above. This system shows the usage of Principal Component Analysis for general data compression. Its dimensional reduction capabilities are further utilized to show its application in Eigenfaces Face recognition algorithm.

### 3. Object categorization using SIFT

- [Project link](http://nbviewer.jupyter.org/gist/kislayabhi/abb68be1b0be7148e7b7)
- This system differentiates between images containing a car, a train and a plane. The category of the image is decided on the basis of SIFT descriptors. K-means clustering is employed for generating bag-of-keypoints and multiclass SVMs are used for the prediction of the category of the object.

### 4. Active Appearance Model

- [Project link](http://nbviewer.jupyter.org/gist/kislayabhi/0cc4f6e6b625873c15de)
- Here I developed a parameterized face needed by the Active Appearance Model (AAM), where the variability of shape and texture is captured from a representative training set. PCA on shape and texture is applied to produce the face model which describes the trained faces with a photorealistic quality.Visit ([here](http://kislayvision.com/research/active-appearance-models/)) for more details.
