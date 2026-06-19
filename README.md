# IOT Security — Steganography with Edge Detection using CNN

This project explores the intersection of deep learning and steganography by implementing an adaptive LSB steganography system on medical CT scans. It uses a custom Convolutional Neural Network (CNN) [...]

## Key Features

- Data pipeline
  - Automated downloading and extraction of the Zenodo CT Spine dataset.
  - Processing into grayscale tensors for training and embedding.

- Custom CNN architecture
  - Conv2D layer initialized with classic Sobel-X and Sobel-Y weights.
  - Trained to adapt these filters while performing binary classification, resulting in edge detection optimized for the dataset.

- Advanced steganography
  - Edge-based embedding: identifies high-intensity edge pixels and masks secret data there rather than in random pixels.
  - Supports both 1st-LSB and 2nd-LSB embedding algorithms.

- Performance metrics
  - Image quality: Peak Signal-to-Noise Ratio (PSNR) and Mean Squared Error (MSE) to measure imperceptibility.
  - Robustness: Bit Error Rate (BER) after introducing synthetic noise to simulate transmission interference.

## Results

- Image quality:
  - 1st-LSB embedding consistently achieved higher PSNR (~74 dB), indicating superior transparency compared to 2nd-LSB (~67 dB).

- Robustness:
  - Under simulated noise, 2nd-LSB showed a lower Bit Error Rate (BER), demonstrating improved resilience to data corruption compared to 1st-LSB.

## Technologies Used

- Frameworks: TensorFlow, Keras
- Libraries: NumPy, Matplotlib, SciPy, OpenCV
- Dataset: CT Spine Dataset (Zenodo)

## Notes

This README summarizes the project's goals, design, and high-level results. If you want, I can:
- Expand this README with installation and usage instructions (requirements, how to run training/embedding/evaluation).
- Commit this formatted README back to the repository (I will confirm the repo/branch before writing).

## Visualization

![Steganography Results](https://github.com/Sayan1733/IOT_Security-_using_steganograpy_with_the-_help_of_edge_detection_using_cnn/raw/main/results_visualization.png)

The visualization above demonstrates the effectiveness of our steganography approach:
- **Original Edge Image**: The input CT scan with edge detection applied
- **Stego Image**: The result after embedding secret data using our edge-based LSB algorithm
- **Embedding Difference**: A magnified view of the pixel-level changes, showing how well the embedded data is concealed within the edge regions
