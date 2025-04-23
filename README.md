# Cross-Architecture-Knowledge-Distillation

## Project Overview
Here is a brief project overview for a GitHub README:

This repository contains a collection of Python scripts for various image processing tasks, including loading and preprocessing the CIFAR-10 dataset, semantic segmentation, superpixelation, and feature extraction. The code also implements neural style transfer using PyTorch and includes functions for loading and preprocessing images, extracting features, and applying style transfer. Additionally, the repository includes scripts for zipping and unzipping folders, calculating folder size and file count, and handling errors related to token limits in AI models.

# Cross-Architecture-Knowledge-Distillation

## Overview
This repository, Cross-Architecture-Knowledge-Distillation, contains the following summarized content based on the files analyzed:

### final_project/cifar_noisy_scrambled_dataset.ipynb
Here is a summary of the content in 2-3 sentences:

The code imports necessary libraries, loads the CIFAR-10 dataset, and applies transformations to the images. It then adds localized noise to the images and saves them to a new directory. Additionally, the code scrambles the images by randomly permuting patches and saves the scrambled images to another directory.

### final_project/cifar_texture_bias_dataset.ipynb
Here is a summary of the content in 3 sentences:

The code consists of various functions and cells for implementing neural style transfer using PyTorch. It includes functions for loading and preprocessing images, extracting features from a VGG model, calculating the Gram matrix, and applying style transfer to a given image. The code also includes cells for testing the style transfer function on a small subset of images, creating partitions of the CIFAR-10 test dataset, and applying style transfer to each partition.

### final_project/final_report.pdf
This error occurs when trying to read a PDF file, specifically "final_report.pdf" in the "final_project" directory. The issue arises because a 'bytes' object is being treated as a file-like object, but it lacks the 'seek' attribute, which is required for file operations.

### final_project/resnet-to-vit.ipynb
Here is a concise summary of the errors and code:

The code encountered errors while summarizing chunks due to exceeding the token limit (6000 TPM) for the `llama3-70b-8192` model in the `on_demand` service tier. The requested tokens ranged from 6291 to 6292, prompting the need to reduce message size or upgrade to the Dev Tier. Meanwhile, the code defines and trains neural network models, fine-tunes and evaluates them, and saves their weights to files.

### final_project/shape_bias_slic_cifar_dataset.ipynb
This code is a collection of Python scripts that perform various image processing tasks, including:

1. **Loading and preprocessing CIFAR-10 dataset**: The code loads the CIFAR-10 dataset, applies data augmentation, and creates a fully convolutional network (FCN) model for semantic segmentation.

2. **Segmenting images using FCN**: The code performs semantic segmentation on the test set using the FCN model and visualizes the results.

3. **Superpixelation using SLIC algorithm**: The code implements the Simple Linear Iterative Clustering (SLIC) algorithm for superpixelation and applies it to the images.

4. **Image processing and feature extraction**: The code performs various image processing tasks, such as resizing, converting to LAB color space, and extracting features using local binary patterns (LBP).

5. **Zip and unzip folders**: The code zips and unzips folders containing images.

6. **Calculating folder size and file count**: The code calculates the size

### final_project/vit-to-resnet.ipynb
Here is a concise summary of the provided context:

The provided code is experiencing a "Request too large" error (Error code: 413) due to exceeding the token limit of 6000 tokens per minute for the `llama3-70b-8192` model in the `on_demand` service tier. The requested tokens are 6291, and the solution is to reduce the message size or upgrade to the Dev Tier.

