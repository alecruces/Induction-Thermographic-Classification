# Induction-Thermographic-Classification

> Using deep learning models to classify thermographic images of induction motors, enabling efficient detection of failure levels.

<p align="center">
<img src="https://github.com/alecruces/Induction-Termographic-Classification/assets/67338986/6d4c9689-da21-4cbe-b3e4-4534b894ce69" alt="image_github" style="width:300px;height:200;"/>
</p>

##  Keywords
Image Classification, GoogleNet, ShuffleNet, Failure Detection, CNN, Computer Vision

---

## Table of Contents

1. [About the Project](#about-the-project)
2. [Key Features](#key-features)
3. [Key Results](#key-results)
4. [Data Overview](#data-overview)
5. [Methodology](#methodology)
6. [Screenshots and Graphs](#screenshots-and-graphs)
7. [Technologies Used](#technologies-used)
8. [Setup & Installation](#setup--installation)
9. [Usage](#usage)
10. [Contributing](#contributing)
11. [License](#license)
12. [Contact](#contact)

---

### 1. About the Project

This project applies deep learning to classify thermographic images of induction motors, detecting varying levels of motor failures. Using GoogleNet and ShuffleNet architectures with transfer learning, the project achieves high classification accuracy, demonstrating that CNNs can be leveraged for industrial fault diagnosis in resource-limited settings.

### 2. Key Features

- **High Accuracy**: Achieved 97% accuracy on the test set for both models.
- **Efficiency with ShuffleNet**: ShuffleNet provides faster training and inference times, ideal for environments with limited computational resources.
- **Transfer Learning**: Enhanced performance by applying pre-trained models, avoiding the need for large datasets or lengthy training from scratch.

### 3. Key Results

- **Model Accuracy**: Both GoogleNet and ShuffleNet achieved 97% accuracy.
- **Efficiency Comparison**:
  - **ShuffleNet**: Faster in both training and inference, suitable for real-time or resource-constrained deployments.
  - **GoogleNet**: High accuracy but requires more computational power.
- **Confusion Matrix**: Both models accurately classified most fault types, with minimal misclassifications.

### 4. Data Overview

The dataset includes thermographic images of induction motors under various fault conditions. Key data points:

- **File**: `IR-Motor-bmp.zip` or `IM_dataset.zip`
- **Image Count**: 369 images, 320x240 resolution, categorized into 11 fault conditions.
- **Classes**: Includes conditions like "No-load" (healthy state), "Fan" failure, "Rotor-0" (locked rotor), and various short-circuit states across motor phases.

### 5. Methodology

This project utilizes two deep learning models optimized for different conditions:

- **GoogleNet**: Known for its balance of accuracy and computational cost, utilizing inception modules to capture features at multiple scales.
- **ShuffleNet**: Lightweight and optimized for faster training and inference, particularly suited for devices with limited processing power.
- **Transfer Learning**: Pre-trained GoogleNet and ShuffleNet models were fine-tuned, significantly reducing computational requirements and achieving high accuracy.

**Hyperparameters**: 
- Both models used the Adam optimizer with batch sizes of 8 (GoogleNet) and 16 (ShuffleNet). No dropout was required, as overfitting was not observed.

### 6. Screenshots and Graphs

These visuals are provided to illustrate data distribution, model performance, and efficiency:

1. **Class Distribution of Faults (Bar Chart)**  
   Shows the number of images per fault type, confirming dataset balance.

   <p align="center">
<img src="https://github.com/alecruces/Induction-Termographic-Classification/assets/67338986/6d4c9689-da21-4cbe-b3e4-4534b894ce69" alt="image_github" style="width:300px;height:200;"/>
</p>

3. **Sample Thermographic Images of Motor Faults**  
   Examples of heat distributions under "Fan" failure and "Rotor-0" (locked rotor) conditions.
<p align="center">
<img src="thermographic_samples" src="https://github.com/user-attachments/assets/6dbd0829-5f2d-4373-95ab-1506475ed7a2" alt="image_github" style="width:300px;height:200;"/>
</p>

3. **Model Accuracy Comparison (Bar Chart)**  
   Comparison of test accuracy between GoogleNet, ShuffleNet, and previous models (e.g., ResNet50).
  <p align="center">
<img src="thermographic_samples" src="[https://github.com/user-attachments/assets/6dbd0829-5f2d-4373-95ab-1506475ed7a2](https://github.com/user-attachments/assets/9612b7b3-2e9a-47a8-9ecd-96e0129b0b72)" alt="image_github" style="width:300px;height:200;"/>
</p>

4. **Confusion Matrix (Heatmap)**  
   Displays classification accuracy across fault classes for GoogleNet and ShuffleNet, showing minimal misclassifications.

   ![Confusion Matrix](path/to/confusion_matrix.png)

5. **Training and Validation Loss Over Epochs (Line Chart)**  
   Loss curves for both GoogleNet and ShuffleNet, showing training stability and convergence.

   ![Loss Curves](path/to/loss_curves.png)

6. **Efficiency Comparison of Models (Bar Chart)**  
   Compares training and inference times per epoch for GoogleNet and ShuffleNet, highlighting ShuffleNet's speed advantage.

   ![Efficiency Comparison](path/to/efficiency_comparison.png)

### 🛠️ Technologies Used

> Emphasizing the primary tools and libraries utilized.

- ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white): Main programming language.
- **🔥 PyTorch**: Used for implementing and training the deep learning models.
- **📊 Transfer Learning**: Leveraged pre-trained GoogleNet and ShuffleNet architectures for efficient training.

### 8. Setup & Installation

Clone the repository and install the required dependencies to run the project:

```bash
# Clone the repository
git clone https://github.com/username/Induction-Thermographic-Classification.git

# Navigate to the project directory
cd Induction-Thermographic-Classification

# Install dependencies
pip install -r requirements.txt
