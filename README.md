This project explores the intersection of Deep Learning and Steganography. It implements a custom Convolutional Neural Network (CNN) designed to perform edge detection using trainable Sobel filters on medical imaging data (CT Spine dataset). The resulting edge maps are then used as a cover for hiding secret messages using Least Significant Bit (LSB) steganography, comparing the performance and robustness of 1st-LSB vs. 2nd-LSB techniques.

Key Features
Data Pipeline: Automated downloading and extraction of the Zenodo CT Spine dataset, processed into grayscale tensors.
Custom CNN Architecture:
Initialized a Conv2D layer with classic Sobel-X and Sobel-Y weights.
Trained the model to adapt these filters while performing binary classification, resulting in edge-detection optimized for the specific dataset features.
Advanced Steganography:
Edge-Based Embedding: Instead of hiding data in random pixels, the system identifies high-intensity edge pixels to mask the presence of secret data.
LSB Comparison: Implemented both 1st and 2nd LSB embedding algorithms.
Performance Metrics:
Image Quality: Calculated Peak Signal-to-Noise Ratio (PSNR) and Mean Squared Error (MSE) to measure imperceptibility.
Robustness: Analyzed the Bit Error Rate (BER) after introducing synthetic noise to simulate transmission interference.
Results
Image Quality: 1st-LSB embedding consistently achieved higher PSNR (74dB), indicating superior transparency compared to 2nd-LSB (67dB).
Robustness: When noise was introduced, 2nd-LSB showed a lower Bit Error Rate (BER), proving to be more resilient to data corruption than 1st-LSB.
Technologies Used
Frameworks: TensorFlow, Keras
Libraries: NumPy, Matplotlib, Scipy, OpenCV
Dataset: CT Spine Dataset (Zenodo)
