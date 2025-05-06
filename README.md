# GC-SWGAN
Semi-Supervised Wasserstein GAN for Galaxy Classification
This code focuses on galaxy morphology classification and implements a semi-supervised learning model, GC-SWGAN, designed to address challenges in galaxy classification when labeled data is limited.

1）Model Overview

The code combines semi-supervised generative adversarial networks (SGAN) with Wasserstein GANs with gradient penalty (WGAN-GP) to create a multi-task learning framework. Within this framework, the discriminator and classifier are independently designed but share part of their architecture. Through collaboration with the generator, the model significantly enhances classification performance and sample generation capabilities while improving convergence and stability during training.

For detailed explanations of the code, please refer to our paper: https://arxiv.org/abs/2504.00500v1

2）Installation Dependencies
This project is developed using Keras and TensorFlow 2 libraries and uses NVIDIA L40S GPU platforms for accelerated training. To install the required dependencies, use the following command:

pip install -r requirements.txt  

Ensure your environment is properly configured to support GPU acceleration.

3）Data Preparation
Before running the code, please download the Galaxy10 DECaLS dataset and unlabeled DECaLS images from the specified website and convert them into h5py format files. Name the files as follows: Galaxy10_DECaLS.h5 and decals_images.h5.

4）Model Training
To start training, run the following script:

python GC-SWGAN.py  

You can adjust the training parameters (e.g., batch size, learning rate) according to your needs. During training, the model optimizes the generator, discriminator, and classifier at different stages.

5）Model Evaluation
After the training is completed, the model's performance metrics will be automatically displayed on the screen.

