# **Comparison of Loss Functions in GANs (LSGAN, WGAN, WGAN-GP)**

## **Overview**
This repository presents a comparative analysis of different loss functions in Generative Adversarial Networks (GANs), including:
- **Least Squares GAN (LSGAN)**
- **Wasserstein GAN (WGAN)**
- **Wasserstein GAN with Gradient Penalty (WGAN-GP)**

The goal is to analyze the impact of different loss functions on the quality of generated images using **Fréchet Inception Distance (FID)** and **Inception Score (IS)**.

## **Implemented GANs**
1. **LSGAN:** Uses least squares loss instead of binary cross-entropy, aiming for more stable training.
2. **WGAN:** Uses Wasserstein distance with weight clipping to improve training stability.
3. **WGAN-GP:** Introduces a gradient penalty term to improve the training of WGAN.

## **Evaluation Metrics**
- **Fréchet Inception Distance (FID):** Lower values indicate better image quality.
- **Inception Score (IS):** Higher values indicate better diversity and realism.

### **Results**
| Model      | Epochs | FID Score ↓ | Inception Score ↑ |
|------------|--------|------------|-------------------|
| **LSGAN**  | 50     | **310.50**  | 1.1300 ± 0.0288  |
| **WGAN**   | 20     | 409.40      | 1.0486 ± 0.0039  |
| **WGAN-GP**| 20     | 323.75      | **1.2083** ± 0.0276 |

### **Key Observations**
- **LSGAN achieved the best FID score (310.50),** suggesting that it produces the most visually realistic images.
- **WGAN-GP had the best Inception Score (1.2083),** meaning it generated more diverse images.
- **WGAN performed the worst in both FID and IS,** possibly due to weight clipping limitations.

## **Installation & Usage**
### **Requirements**
Ensure you have Python and the required dependencies installed. Use the following command to install necessary packages:
```bash
pip install torch torchvision numpy matplotlib scipy
```

## **Conclusion**
This comparison highlights the trade-offs between different loss functions in GANs. LSGAN shows the best overall performance in terms of FID, while WGAN-GP produces more diverse images. WGAN's weight clipping limitation may hinder training quality.

## **Author**
Richa Gupta
