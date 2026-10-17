# Google Street View Landmark Recognition

## 1. Project Overview

Google Street View Landmark Recognition is a deep learning project that identifies famous landmarks from images using image classification techniques. The system takes an input image, processes it, and predicts the landmark category based on a trained deep learning model.

This project is developed using Python and Google Colab and demonstrates the application of computer vision and transfer learning for landmark identification.

## 2. Objectives

- Build an image classification model to recognize landmarks.
- Preprocess and prepare landmark images for training.
- Apply deep learning techniques to extract useful image features.
- Predict landmark categories from uploaded images.
- Evaluate model performance using training and validation metrics.
- Demonstrate predictions on multiple images.

## 3. Technologies Used

- **Programming Language:** Python
- **Platform:** Google Colab
- **Deep Learning:** TensorFlow and Keras
- **Model Approach:** Transfer learning with MobileNetV2, if used in the notebook
- **Image Processing:** Pillow and NumPy
- **Data Visualization:** Matplotlib
- **Dataset:** Landmark image dataset downloaded or prepared using `download-dataset.sh`

## 4. Project Workflow

1. **Dataset preparation:** Download and organize landmark images.
2. **Data preprocessing:** Resize images and prepare them for model input.
3. **Dataset splitting:** Separate the images into training and validation sets.
4. **Model development:** Build an image classification model using a CNN or transfer learning.
5. **Model training:** Train the model on labeled landmark images.
6. **Prediction:** Upload new landmark images and predict their classes.
7. **Evaluation:** Review training accuracy, validation accuracy, and other suitable metrics.
8. **Model saving:** Save the trained model for future use.

## 5. Dataset

The project uses a dataset containing images of landmarks organized into categories.

The dataset preparation script is named `download-dataset.sh`. The actual dataset source, number of images, and landmark classes should be documented according to the dataset downloaded in Google Colab.

**Dataset details to add:**
- Dataset source: [Add the actual source or URL]
- Number of landmark classes: [Add actual count]
- Number of training images: [Add actual count]
- Number of validation/test images: [Add actual count]

## 6. Installation and Setup

The project is designed to run in Google Colab.

### Step 1: Open Google Colab

Visit https://colab.research.google.com/ and create a new notebook.

### Step 2: Install Dependencies

```python
!pip install tensorflow pillow numpy matplotlib
```

### Step 3: Prepare the Dataset

Upload or run the provided `download-dataset.sh` script according to its instructions. Ensure that the dataset is downloaded and extracted successfully.

### Step 4: Train the Model

Run the notebook cells in the correct order to preprocess the images, initialize the model, and train it.

### Step 5: Test an Image

```python
from google.colab import files

uploaded = files.upload()

for filename in uploaded:
    predict_landmark(filename)
```

The prediction function must be defined and the trained model must be loaded before running this cell.

## 7. Model Description

The project uses image classification to map an input image to one of the landmark categories learned during training.

If MobileNetV2 transfer learning is used, its pretrained convolutional layers extract visual features, while the classification head learns to distinguish the landmark categories in the project dataset.

The model's output represents predicted class probabilities. The category with the highest predicted probability is selected as the predicted landmark.

## 8. Evaluation

Model performance should be assessed using the actual results produced during training and testing.

Recommended evaluation measures include:

- **Training accuracy:** Measures classification accuracy on training data.
- **Validation accuracy:** Measures classification accuracy on validation data.
- **Precision:** Measures the proportion of correct positive predictions for a class.
- **Recall:** Measures the proportion of actual examples of a class correctly identified.
- **F1-score:** Balances precision and recall.
- **Confusion matrix:** Shows correct and incorrect predictions across classes.

Actual metric values should be added after evaluation. Predictions on randomly uploaded images alone do not establish the model's overall accuracy.

## 9. Applications

- Identification of famous landmarks from photographs.
- Tourism and travel information systems.
- Educational applications for learning about landmarks.
- Image-based cultural heritage exploration.
- Computer vision research and experimentation.

## 10. Limitations

- The model can recognize only the landmark classes represented in its training labels.
- Prediction quality depends on dataset size, image quality, and class balance.
- Images with unusual angles, poor lighting, or heavy obstruction may be misclassified.
- A predicted class is not guaranteed to be correct.
- Performance on unseen landmarks may be poor if they are not included in training.

## 11. Future Enhancements

- Expand the dataset with additional landmark classes.
- Improve generalization using data augmentation.
- Evaluate the model using a separate labeled test set.
- Add top-3 predictions with confidence scores.
- Develop a web interface for image uploads and predictions.
- Deploy the model as an API or web application.
- Improve performance using further model tuning and error analysis.

## 12. Conclusion

The Google Street View Landmark Recognition project demonstrates how deep learning and computer vision can be applied to landmark image classification. By preparing a labeled image dataset, training a classification model, and testing it with uploaded images, the project provides a practical introduction to image recognition.

The project can be extended through improved datasets, systematic evaluation, and deployment as an interactive landmark recognition application.

## 13. Author

**Project:** Google Street View Landmark Recognition  
**Platform:** Google Colab  
**Domain:** Deep Learning and Computer Vision  
**Developed as part of:** GUVI Project Work
