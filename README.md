# Predicting Facial Expression
_________
## Context:

Emotion and facial expression recognition through machine learning plays a pivotal role in numerous applications across various domains. It facilitates more intuitive human-computer interactions, enhances customer experiences, aids in mental health monitoring, and improves educational methods. Additionally, it has practical implications in marketing, healthcare, security, and accessibility. This technology provides insights into human emotions and behavior, offering valuable data for research and decision-making. 

## Problem Statement

The objective of this project is to construct a Convolutional Neural Network (CNN) model capable of analyzing images of individuals exhibiting different facial expressions. The primary goal is to achieve a minimum accuracy of 70% on both the training and testing datasets, effectively classifying these expressions into their respective emotion categories. To accomplish this, I will use a combination of [.jpg](https://www.kaggle.com/datasets/msambare/fer2013) and [.csv](https://www.kaggle.com/datasets/deadskull7/fer2013) data sourced from the FER2013 dataset. In cases where the FER2013 dataset proves insufficient for accurate facial expression recognition, I will consider transitioning to the [CK+ dataset](https://www.kaggle.com/datasets/davilsena/ckdataset). The FER2013 dataset comprises emotion classes such as Angry, Fear, Happy, Sad, Surprised, and Neutral, while the CK+ dataset includes the classes of Anger, Disgust, Fear, Happiness, Sadness, Surprise, Neutral, and Contempt. This project aims to develop a robust and accurate model for emotion and facial expression recognition.
__________________

## Evaluation, Conclusions, Recommendations, and Future Steps

### Evaluation:

In attempt of achieving a model with 70% accuracy on both training and testing sets, multiple iterations were conducted using different datasets and model configurations. The initial attempt with the .jpg FER2013 dataset, utilizing a basic CNN with no early stopping or data augmentation, yielded unsatisfactory results, with a training accuracy of 0.61 and a testing accuracy of 0.51 after 5 epochs. Subsequent modifications, including an extended training period, showed improvements in training accuracy but limited progress in testing accuracy, ultimately leading to overfitting.

Transitioning to the FER2013 dataset in CSV format, another basic CNN model was trained, resulting in a training accuracy of approximately 0.57 and a testing accuracy of about 0.53. Although the previous model showed better testing accuracy (~0.70), this model demonstrated reduced variance, indicating potential for improvement.

Further experimentation by extended the training of the previous model to 25 epochs did not meet the desired criteria, yielding a training accuracy of about 0.73 and a testing accuracy of about 0.54, with noticeable overfitting. Incorporating early stopping and additional convolutional layers did not significantly alleviate overfitting, resulting in a training accuracy of 0.65 and a testing accuracy of 0.56. Attempting regularization to address overfitting led to reduced performance, with training and testing accuracies both reaching only 0.25.

Given the challenges encountered with the FER2013 dataset, I decided to move on to the CK+ dataset, tailored for facial expression analysis. Initial modeling with the CK+ dataset demonstrated considerable improvement, achieving a training accuracy of about 0.87 and a testing accuracy of about 0.86. Subsequently, increasing the number of epochs and adding convolutional layers further enhanced the model's performance, achieving a peak training accuracy of approximately 0.90 and a testing accuracy of about 0.85 in epoch 29. These results far surpassed the 70% accuracy threshold on both training and testing sets, while maintaining favorable variance characteristics.

The shift to the CK+ dataset proved successful in achieving the project's accuracy objectives, highlighting the dataset's suitability for facial expression recognition.


### Conclusion and Recommendations:

The project's attempt to predict facial expressions and emotions from images revealed several valuable insights. While initial attempts using the FER2013 dataset with .jpg and .csv formats faced challenges in meeting the desired 70% accuracy on both training and testing sets, they provided valuable lessons in dealing with overfitting, dataset limitations, and model complexity.

Transitioning to the CK+ dataset proved to be a worthwhile decision, resulting in significantly improved model performance. The CK+ dataset, designed specifically for facial expression analysis, showcased its superiority in providing accurate predictions and better handling of overfitting issues.

In terms of recommendations gained from this project, firstly, it's appears to be crucial to carefully consider the dataset used. Specialized datasets, such as CK+, tailored explicitly for facial expression analysis, have appeared to yield superior results compared to more generalized datasets like FER2013. Secondly, the complexity of the model and hyperparameter settings should be somewhat approached with caution. Striking the right balance can be essential to avoid overfitting while maximizing accuracy. Lastly, consider the use of early stopping with monitoring of validation loss to prevent overfitting and save valuable training time, as some of these models can take hours to fit.

### Future Steps:

The project's success with the CK+ dataset opens up exciting opportunities and real-world applications of the trained model, such as integrating it into human-computer interaction systems, healthcare applications, or marketing analytics. Collecting additional data from diverse sources can enhance the model's ability to recognize a broader range of facial expressions, potentially leading to more robust results. Continuously staying updated with the latest advancements in facial expression recognition and machine learning may prove to be vital, allowing us to incorporate cutting-edge techniques into future iterations of the model and keep our research at the forefront of this rapidly evolving field.