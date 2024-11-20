## Business Understanding
This project aims to automate the detection of pneumonia from chest X-ray images using a convolutional neural network (CNN) model. Pneumonia, if not diagnosed early, can lead to severe complications and increased mortality, especially among vulnerable populations. Automated detection systems can assist healthcare professionals by providing faster and more accurate diagnosis, reducing workloads, and supporting regions with limited access to radiology experts.

## Data Understanding
The dataset used is the “Chest X-Ray Images (Pneumonia)” from Kaggle (https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia), consisting of 5,863 images divided into two categories: Normal and Pneumonia. This dataset includes pediatric chest X-rays, with pneumonia cases labeled as either viral or bacterial. The dataset is structured into training, validation, and testing sets to facilitate model development and evaluation.

## Data Preparation
Data preparation involved several key steps to ensure the dataset was ready for modeling. I created organized directories for the images, ensuring they were structured correctly for efficient access during the modeling process. These steps collectively prepared the images for effective training and evaluation of the model.

## Exploratory Data Analysis
EDA reveals class imbalances in the dataset, with more pneumonia cases than normal images. Visual inspections of X-rays highlight differences between normal and infected lungs, such as increased opacity in pneumonia-affected areas. Basic statistics such as class distributions and average pixel intensities guide data augmentation and model strategy. I implemented data augmentation techniques to enhance the diversity of the training images. 

## Modeling
**Model 1:** This basic CNN architecture achieved a precision of 0.90 and a recall of 0.86, indicating good performance but missing some pneumonia cases.
**Model 2:** Enhanced with additional convolutional layers and regularization, this model maximized recall at 0.99 but suffered from low precision (0.69), resulting in a high number of false positives.
**Model 3:** This optimized CNN incorporated batch normalization and dynamic learning rate scheduling, achieving a balanced performance with a precision of 0.87, recall of 0.94, and an F1 score of 0.90.

## Evaluation:
**Final Model:** The final model demonstrated an accuracy of approximately 85.7%, with 189 true positives and 346 true negatives, while highlighting the need for improvement due to 44 false negatives.

## Conclusion
In this project, we developed a robust CNN model to classify X-ray images of pneumonia and healthy lungs, addressing a critical healthcare challenge. Through iterative improvements across three models, we enhanced performance metrics such as precision and recall, ultimately achieving a balanced final model that minimizes false negatives while maintaining high accuracy. The insights gained from this work not only demonstrate the potential of deep learning in medical diagnostics but also highlight the importance of ongoing refinement and evaluation to ensure effective real-world applications. Future work will focus on further reducing false negatives and improving model generalization.

## Limitations
- Firstly, the dataset does not fully represent the diversity of pneumonia cases encountered in real-world clinical settings, potentially affecting the model’s generalizability.
- Additionally, the class imbalance, with significantly more pneumonia cases than normal cases, could lead to biased predictions, particularly in identifying healthy patients.
- Finally, while the model shows promising results, further validation on external datasets is necessary to ensure its reliability in clinical applications.

## Recommendations and Next Steps
-Expanding the dataset to include a more diverse range of X-ray images from various demographics and clinical backgrounds would improve the model’s generalizability.
Implementing advanced techniques such as transfer learning could also enhance performance, particularly in addressing class imbalance. 
-Further exploration of ensemble methods may yield better predictive accuracy by combining the strengths of multiple models. It is crucial to conduct extensive validation on external datasets to assess the model’s robustness in real-world scenarios. 
-Integrating additional clinical data, such as patient history and symptoms, could provide a more comprehensive diagnostic tool, ultimately improving patient outcomes.

## More Information:
Find the full analysis in the CNN_Pneumonia_Classifier.ipynb or review this [presentation](CNNPneumoniaClassifier.pdf).

## Repository Structure
- Graphs
- README.md
- CNN_Pneumonia_Classifier.ipynb
- CNNPneumoniaClassifier.pdf

### Author: Adriana Ramirez Franco (aramirezfr20@gmail.com)
