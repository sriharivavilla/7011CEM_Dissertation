# 7011CEM_Dissertation

# Comparison of ML and CNN with Advanced Sparse Compressive Techniques for Image Reconstruction

Author: Srihari Reddy Vavilla
Student ID: 16223143
Supervisor: Dr. Amjad Saeed Khan

# 1. Project Overview

This dissertation presents a comparative study of machine learning models and advanced sparse compressive sensing techniques for image reconstruction. The goal is to evaluate how effectively different approaches reconstruct images from limited or compressed data.

The study includes both traditional sparse optimization methods and modern deep learning models. The comparison focuses on reconstruction quality, perceptual similarity, and computational efficiency.

# 2. Techniques Used

The project evaluates four main approaches:

2.1 LASSO

LASSO is a sparse regression method that reconstructs images by enforcing sparsity in the transform domain. It is effective for simple structures but struggles with complex textures.

2.2 FISTA

FISTA is an accelerated optimization algorithm that improves convergence speed compared to LASSO. However, it may still produce blurry reconstructions.

2.3 Sparse Autoencoder (SAE)

This is an advanced machine learning approach that combines sparse representation with deep learning. It captures nonlinear patterns and produces high-quality reconstructions.

2.4 Convolutional Neural Network (CNN)

CNN is a deep learning model that learns spatial features directly from images. It provides balanced performance in terms of reconstruction quality and speed.

# 3. Dataset

The project uses the DIV2K dataset, which consists of high-resolution images.

Training images: 800
Validation images: 100
Images are converted to grayscale and resized to 128 x 128
Pixel values are normalized between 0 and 1

Dataset Source :
https://data.vision.ee.ethz.ch/cvl/DIV2K/

The dataset provides diverse textures and structures suitable for evaluating reconstruction techniques.

# 4. Evaluation Metrics

The performance of each model is measured using the following metrics:

PSNR (Peak Signal-to-Noise Ratio): Measures reconstruction quality. Higher is better.
SSIM (Structural Similarity Index): Measures structural similarity. Higher is better.
LPIPS (Perceptual Similarity): Measures visual similarity. Lower is better.
Time: Measures computational efficiency. Lower is better.
# 5. Results Summary

Final comparative results are as follows:

LASSO: PSNR 20.58, SSIM 0.54, LPIPS 0.27, Time 0.49
FISTA: PSNR 19.70, SSIM 0.41, LPIPS 0.40, Time 0.85
SAE: PSNR 22.70, SSIM 0.70, LPIPS 0.19, Time 0.14
CNN: PSNR 20.00, SSIM 0.61, LPIPS 0.23, Time 0.16
# 6. Analysis of Results

SAE achieved the best performance across all metrics. It produced the highest PSNR and SSIM values and the lowest LPIPS score, indicating superior reconstruction quality and perceptual accuracy. It was also the fastest method.

CNN showed good performance with balanced results. It provided better perceptual quality than traditional methods but did not outperform the SAE model.

LASSO performed moderately well but lacked the ability to reconstruct fine details.

FISTA had the lowest performance, with reduced image quality and higher computation time.

# 7. Key Findings
Deep learning methods outperform traditional sparse techniques
SAE is the most effective model for image reconstruction
CNN provides a good trade-off between accuracy and efficiency
Sparse optimization methods are limited in handling complex image structures
# 8. Conclusion

This dissertation demonstrates that advanced machine learning techniques significantly improve image reconstruction performance.

Residual Sparse Autoencoders provide the best results due to their ability to learn complex patterns and maintain sparsity. CNN models also perform well but are slightly less accurate.

Traditional methods like LASSO and FISTA are less effective for modern image reconstruction tasks.

# 9. How to Run the Project
Install required libraries such as numpy, torch, opencv, matplotlib, and lpips
Download the DIV2K dataset
Run preprocessing to resize and normalize images
Train or load models (LASSO, FISTA, SAE, CNN)
Evaluate using PSNR, SSIM, LPIPS
Compare results
