# Breast Tumor Classification Using Histopathological Images

## Project Overview

This project focuses on the classification of breast tumor tissues as benign or malignant using **Convolutional Neural Networks (CNNs)**. The models are developed and evaluated on the **BreakHis** dataset, which contains histopathological images of breast tumor tissues at various magnifications.

### Research Questions
1. Can CNN architectures (e.g., VGG16, ResNet50, and EfficientNet) accurately classify benign vs malignant tumor tissue images using the BreakHis dataset?
2. Which visual features (texture, shape, patterns) are most influential in classification?
3. How does performance vary across different image magnifications (200×, 400×), and can models generalize across magnification levels?

## Dataset Information

- **Dataset Name**: BreakHis – Breast Cancer Histopathological Database
- **Source**: [Mendeley Data – BreakHis Dataset](https://data.mendeley.com/datasets/jxwvdwhpc2/1)
- **Contributors**: Mayke Pereira et al., Instituto Federal de Educação, Ciência e Tecnologia do Espírito Santo, Brazil
- **Data Type**: RGB images (224 × 224 px) of breast-tumor tissues at magnifications 40×, 100×, 200×, 400×
- **Labels**: Benign (0) / Malignant (1)

## Setup and Installation

Follow these steps to set up the project:

1. Clone the repository:
   ```bash
   git clone https://github.com/st24aaq/breast-tumor-classification.git
   cd breast-tumor-classification
   ```

2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Download the **BreakHis** dataset using the provided script:
   ```python
   !apt-get install wget -q
   !wget -O breakhis.zip "https://prod-dcd-datasets-cache-zipfiles.s3.eu-west-1.amazonaws.com/jxwvdwhpc2-1.zip"
   !unzip -q breakhis.zip -d /content/breakhis_dataset
   ```

## Code Description

### 1. **Data Download and Setup**:
The project begins by downloading the **BreakHis** dataset using the `wget` tool and unzipping it for further use. This ensures the images are available for model training.

### 2. **Image Count Summary**:
The notebook provides a summary of image counts for benign and malignant images at two magnifications (200X and 400X) to help understand the dataset distribution.

### 3. **CNN Model Setup**:
The project uses various CNN architectures (VGG16, ResNet50, EfficientNet) for training and classification. The models are defined, compiled, and trained using TensorFlow and Keras.

### 4. **Evaluation and Explanation**:
The notebook includes evaluation metrics and model explainability methods (e.g., Grad-CAM, LIME) to provide insights into which image features contribute to classification.

## How to Run

After setting up the environment and downloading the dataset, run the notebook cells sequentially to train the models, evaluate them, and visualize the results.

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- BreakHis dataset contributors
- TensorFlow and Keras for deep learning model development
