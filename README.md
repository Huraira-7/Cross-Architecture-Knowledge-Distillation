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


🧠 Cross-Architecture Knowledge Distillation
Can We Induce Desirable Properties into Models via Cross-Architecture Knowledge Distillation?
Authors: Muhammad Huraira Anwer, Adeen Ali Khan – LUMS, Pakistan

🚀 Overview
In this project, we explored whether key inductive biases (like shape bias, locality, and permutation invariance) can be transferred across different neural network architectures using knowledge distillation (KD).

More specifically, we focused on distilling attention-based Vision Transformers (ViT) into convolutional models (CNNs) and vice versa—something that's rarely studied. Our goal was to see not just if performance transfers, but if model behavior and biases do too.

🎯 Objectives
We structured our work around three guiding questions:

Can architectural biases (e.g., shape, texture, locality) be transferred through KD across ViTs and CNNs?

Do transformer properties like permutation invariance survive in student CNNs?

How do various distillation methods affect the efficiency and behavior of students under noisy and perturbed inputs?

🏗️ What We Did
We created custom test datasets with stylized textures, scrambled patches, and added noise to stress-test learned biases.

We designed two major pipelines:

CNN ➡️ ViT Distillation using methods like CSKD and VLFKD.

ViT ➡️ CNN Distillation using methods like CRD, SSKD, and CAPD.

To control compute costs, all models were trained on CIFAR-10 under limited epochs (≤ 5).

We evaluated each model on accuracy as well as bias metrics that quantify model reliance on texture, shape, or global structure.

🔍 Key Design Decisions
Separate distillation methods were chosen based on architecture direction (CNN-to-ViT vs ViT-to-CNN), due to incompatible feature representations.

We used baseline "independent" models (trained without a teacher) to judge how much actual knowledge was transferred.

We explicitly limited training epochs to simulate low-compute deployment settings, emphasizing practical feasibility over perfect accuracy.

📊 Highlights & Insights
CNN ➡️ ViT
CSKD emerged as the most efficient and effective method, excelling in transferring texture bias and noise robustness.

However, ViTs struggled to inherit CNN's locality bias, and improvements over the independent baseline were mild.

Suggests CNNs may be inherently less effective as teachers for behavior-focused distillation.

ViT ➡️ CNN
CRD and SSKD were both effective at instilling shape bias and permutation invariance into student CNNs.

The improvements were significant compared to the independent baseline—highlighting the power of ViTs as behavior-rich teachers.

Despite higher compute costs, these methods offer promising robustness gains for real-world deployment.

⛓️ Limitations
We operated under strict training budgets (≤ 5 epochs), which likely capped the full potential of the distillation methods.

Some methods like CAPD underperformed simply because they didn’t converge under such limited training.

Future work should explore:

Longer training schedules

Broader datasets

Mechanisms to avoid "over-distilling" undesirable properties (e.g., ViT’s weak texture awareness into CNNs)

💡 Takeaways
ViTs make powerful teachers, capable of transferring abstract, global properties like permutation invariance.

CNNs are efficient learners, but might struggle to adopt attention-like behaviors unless the method is designed very carefully.

Cross-architecture KD isn't just viable—it can yield more robust, generalizable models when done thoughtfully.
