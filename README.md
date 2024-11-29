# Project : Emotion recognition
## Project results and overview
I have decided to do this project for everyone to be able to recognize human emotions. 
I developed a robust model for recognizing human emotions from facial images using the YOLOv8 framework. 
I wanted to advance human-computer interaction and provide meaningful insights into emotion-based applications such as healthcare, security, and user experience design.

The key objectives were first to train a YOLOv8 model to classify facial images in seven several emotion categories: angry, disgust, fear, happy, neutral, sad, surprise.
The second key objective was to evaluate the model's performance in terms of accuracy and confusion metrics.
Finally, we wanted to optimize training to handle dataset imbalances and improve recognition for underperforming classes.

The model achieved a training accuracy of ~83% for the "happy" class, while other classes like "disgust" and "sad" performed poorly due to dataset imbalance and subtle differences between emotions.
The final model demonstrates 34% overall accuracy on the test datase which can be good for the beginning of a project.
Unfortunately the accuracy could have been better, but due to some vectors like some issues with collab or too much time lost in the training the accuracy is low.

## Source code 

## Performance metrics
To observe the result of my training model we will use a Confusion Matrix.
The confusion matrix illustrates the performance of the trained YOLO model in classifying emotions. 
Each cell represents the number of predictions made for a particular class compared to the actual labels.

In the matrix there is "Happy" which the most accurately predicted emotion, with 1,479 correct predictions out of 1,774 samples (recall = 0.83).
Moreover, there is "Disgust" which has the lowest prediction accuracy, with almost no correct classifications, indicating the model struggles significantly with this class.
Classes like "Angry" and "Fear" show moderate prediction performance but with notable misclassifications across other emotions.
![image](https://github.com/user-attachments/assets/1693daf9-d378-4945-a1ae-93dfd69c9323)

I also wanted to evaluate the performance of my model using the classification report which provides a detailed breakdown of the model's precision, recall, and F1-score for each class. These metrics are defined as follows:
Precision: Proportion of correct positive predictions out of all positive predictions made.
Recall: Proportion of actual positives correctly predicted by the model.
F1-score: Harmonic mean of precision and recall, providing a balance between the two.
Performance breakdown:
The highest emotion performance is "Happy" which achieved the highest scores across all metrics (precision, recall, F1-score = 0.83), reflecting the model's ability to classify this class effectively.
We have then the moderate performance with "Angry" (F1-score = 0.50) and "Fear" (F1-score = 0.27) show acceptable performance but require further improvement to reduce misclassifications.
Finally, we have poor performance like "Neutral" (F1-score = 0.13), "Sad" (F1-score = 0.03), and "Surprise" (F1-score = 0.03) show very low accuracy.
"Disgust" fails completely with an F1-score of 0.00.
Observations:
The imbalance in class accuracy suggests that the model needs further tuning, such as:
Addressing class imbalance during training.
Incorporating additional features or augmenting the dataset to better represent subtle differences between certain emotions.
![image](https://github.com/user-attachments/assets/cbf21c53-68c0-4af9-b555-e8f1a5e7fc35)

## Installation and usage
For installing and running the project, we first need to respect this requiemremnts: having Python 3.8+, PyTorch, Ultralytics YOLOv8 and uses Google Colab

## References and documentation

## Issues and contribution

## Future work 
For this project i see a lot of things to upgrade in the future. 
First is the Class Balancing. We will need to increase the representation of underperforming classes using synthetic data or data augmentation techniques.
Next would be the Improved Architectures. We will experiment with other architectures such as EfficientNet or ResNet for emotion recognition.
Finally it will be the Real-world Deployment. Integrate the model into an application, such as a live emotion recognition system using webcam input.
