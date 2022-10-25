# Rock Classification using CNN
Classify six types of rock using a Convolutional Neural Network.

## Prologue
Rock classification is a fundamental part of geological surveys. However, accurate classification of rock is still challenging considering the high variety of rock types and the nonuniformity of their properties. Therefore, I present a method to classify six types of rocks. 

# What It Is
This project can classify high similarity six types of rock with accuracy of 93% and show the results with a saliency map highlighting the discriminative object parts detected by the CNN.


# Dataset
The [SDNet2018](https://digitalcommons.usu.edu/all_datasets/48/) dataset is the benchmark for crack detection which contains over 56,000 images of six types of rock: cracked and uncracked concrete bridge decks, walls, pavements, respectively. The dataset includes cracks as narrow as 0.06 mm and as wide as 25 mm with a variety of obstructions, including shadows, surface roughness, scaling, edges, holes, and background debris. Each image is segmented into 256 *256 pixels sub images for later uses.


# How It Works
1. This project uses ResNet50 to achieve an accuracy of 93%. I used data augmentation and conditioned the selection of the best model on the accuracy of the validation set to prevent over-training. Moreover, transfer learning was applied to all classifiers when pre-trained on the ImageNet dataset.

2. Since class activation maps could localize the object, three various saliency maps (Grad-CAM, Grad-CAM++, Score-CAM) were performed on the dataset. Even though Grad-CAM++ and Score-Cam both can locate multiple objects even under occlusion, Score-CAM was more focused than Grad-CAM++.

