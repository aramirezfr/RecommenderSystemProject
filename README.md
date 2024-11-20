# Business Understanding
This project aims to automate the detection of pneumonia from chest X-ray images using a convolutional neural network (CNN) model. Pneumonia, if not diagnosed early, can lead to severe complications and increased mortality, especially among vulnerable populations. Automated detection systems can assist healthcare professionals by providing faster and more accurate diagnosis, reducing workloads, and supporting regions with limited access to radiology experts.

# Data Understanding
The dataset used is the “Chest X-Ray Images (Pneumonia)” from Kaggle (https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia), consisting of 5,863 images divided into two categories: Normal and Pneumonia. This dataset includes pediatric chest X-rays, with pneumonia cases labeled as either viral or bacterial. The dataset is structured into training, validation, and testing sets to facilitate model development and evaluation.

## Data Preparation
Data preparation involved several key steps to ensure the dataset was ready for modeling. I created organized directories for the images, ensuring they were structured correctly for efficient access during the modeling process. These steps collectively prepared the images for effective training and evaluation of the model.

# Exploratory Data Analysis
EDA reveals class imbalances in the dataset, with more pneumonia cases than normal images. Visual inspections of X-rays highlight differences between normal and infected lungs, such as increased opacity in pneumonia-affected areas. Basic statistics such as class distributions and average pixel intensities guide data augmentation and model strategy. I implemented data augmentation techniques to enhance the diversity of the training images. 

## Modeling
**Model 1:** This basic CNN architecture achieved a precision of 0.90 and a recall of 0.86, indicating good performance but missing some pneumonia cases.
**Model 2:** Enhanced with additional convolutional layers and regularization, this model maximized recall at 0.99 but suffered from low precision (0.69), resulting in a high number of false positives.
**Model 3:** This optimized CNN incorporated batch normalization and dynamic learning rate scheduling, achieving a balanced performance with a precision of 0.87, recall of 0.94, and an F1 score of 0.90.

## Evaluation:
**Final Model:** The final model demonstrated an accuracy of approximately 85.7%, with 189 true positives and 346 true negatives, while highlighting the need for improvement due to 44 false negatives.

# Conclusion
The project demonstrates the potential of CNNs in automating pneumonia detection. It offers a valuable diagnostic aid to healthcare professionals.

## Limitations
- The dataset is focused primarily on pediatric cases and may not generalize well to adult populations.
- Imbalanced data between normal and pneumonia cases could affect model performance, requiring strategies such as oversampling or weighted loss functions.
- X-ray images alone may not be sufficient for conclusive diagnosis, as clinical factors are also essential in real-world scenarios.

## Recommendations and Next Steps
- Improve model generalization by adding more diverse X-ray datasets, including adult cases and different pneumonia types.
- Deploy the model in a clinical setting as a decision-support tool and collect feedback for iterative improvements.

