# Cross-Architecture-Knowledge-Distillation

## Project Overview
This project explores the application of deep learning techniques to image processing and analysis tasks, including dataset preparation, knowledge distillation, and semantic segmentation. The code implements various PyTorch models and techniques, such as Vision Transformers and convolutional models, to perform tasks like image classification, style transfer, and superpixelation. The project's goal is to develop and evaluate robust models that can effectively transfer knowledge and adapt to noisy data.

# Cross-Architecture-Knowledge-Distillation

## Overview
This repository, Cross-Architecture-Knowledge-Distillation, contains the following summarized content based on the files analyzed:

### final_project/cifar_noisy_scrambled_dataset.ipynb
Here is a concise summary of the code:

The code consists of several sections:

1. **Loading and preprocessing CIFAR-10 dataset**: The code loads the CIFAR-10 dataset, applies data augmentation, and creates data loaders for training and testing.

2. **Localised Noise Injection**: The code defines a function to add localized Gaussian noise to images and applies it to the test dataset.

3. **Scrambling images**: The code defines a function to scramble images by randomly permuting patches and applies it to the test dataset.

4. **Saving and zipping datasets**: The code saves the noisy and scrambled datasets as PNG images and zips them for later use.

5. **Visualizing images**: The code visualizes original, noisy, and scrambled images using matplotlib.

6. **Copying files to Google Drive**: The code copies the zipped datasets to Google Drive.

7. **Loading and displaying images from NumPy arrays**: The code loads an image from a NumPy array

### final_project/cifar_texture_bias_dataset.ipynb
Here is a summary of the code in 2-3 sentences:

The code implements a style transfer model using PyTorch, which takes a content image and a style image as input and generates a styled image. The model uses a pre-trained VGG19 network to extract features from the images and calculates a loss function based on the difference between the features of the styled image and the content image. The code also includes functions for loading and saving images, displaying images, and creating partitions of a dataset for batch processing.

### final_project/final_report.pdf
This project explores cross-architecture knowledge distillation between Vision Transformers and convolutional models, focusing on transferring knowledge and evaluating robustness to noisy data. Various techniques are employed, including Logit Matching, Contrastive Representation Distillation, and Cumulative Spatial Knowledge Distillation, to transfer architectural biases such as shape, texture, and locality. The results show that these methods are effective in transferring desired properties, but further research is needed to prevent the transfer of undesirable properties.

### final_project/resnet-to-vit.ipynb
The code implements knowledge distillation techniques to transfer knowledge from a teacher model to a student model, evaluating their performance on various datasets including CIFAR-10, Texture-Bias, Shape-Bias, and others. The student models are trained using different methods such as Logit Matching, Contrastive Representation Distillation, and Cumulative Spatial Knowledge Distillation. The code defines functions for model creation, fine-tuning, evaluation, and training, and uses these to train and evaluate multiple models on different datasets.

### final_project/shape_bias_slic_cifar_dataset.ipynb
This PyTorch code implements a fully convolutional network (FCN) for semantic segmentation on the CIFAR-10 dataset, performing tasks such as data loading and preprocessing, model definition, segmentation, and visualization. Additionally, it applies the Simple Linear Iterative Clustering (SLIC) algorithm for superpixelation and includes various image processing tasks, including parallel processing, zipping, and calculating folder size.

### final_project/vit-to-resnet.ipynb
The code is a collection of PyTorch scripts for loading, preprocessing, and fine-tuning various image datasets using Vision Transformers and ResNet models. It performs tasks such as loading and extracting zip files, loading and preprocessing image datasets, defining custom datasets and data loaders, and fine-tuning models for image classification tasks. The code also includes functions and classes for knowledge distillation, contrastive learning, and model evaluation.

