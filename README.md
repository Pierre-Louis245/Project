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
For this project, we have first Projet Image understanding. This is where there are best.pt the model I used for this project and fer2013_subset.yaml which is the subset of the dataset used for training.
We have then the folder train_subset were several pictures of every emotion, happy, sad, angry...
The first step for the set up is to clone the git using the command: git clone https://github.com/Pierre-Louis245/Project.git
Then to navigate to the repository use cd Project

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
For installing and running the project, we first need to respect this requiemremnts: having Python 3.8+, PyTorch, Ultralytics YOLOv8 and uses Google Colab.
Then we need to install dependencies with this command: pip install -r requirements.txt.
We then need to create a file in the repository with all necessary dependencies.
We also need to ensure that fer2013_subset.yaml file is in the root directory of the project and best.pt file (trained YOLO model) is also in the root directory.
After the steps before write the code: python detect.py --weights best.pt --data fer2013_subset.yaml --source path_to_image.jpg --conf-thres 0.25
and replace path_to_image.jpg with the path to an image or folder containing images for testing.
To evaluate the model use python val.py --weights best.pt --data fer2013_subset.yaml
This will calculate metrics like precision, recall, and mAP (mean Average Precision) for the validation set defined in the fer2013_subset.yaml file.

## References and documentation
Here is some reference and documentation I used for this project.
FER-2013 Dataset: it is used for emotion recognition tasks and was introduced in the ICML 2013 challenges.
Dataset source: FER-2013 Dataset on Kaggle

YOLO (You Only Look Once) Framework:The project relies on YOLO (You Only Look Once), a family of real-time object detection models. Depending on the version used:
YOLOv5: YOLOv5 GitHub Repository
YOLOv8: YOLOv8 Documentation

PyTorch: is the deep learning framework used to build and train the model.
Documentation: PyTorch Official Documentation

Matplotlib: For plotting graphs and visualizing model performance metrics, Matplotlib is used.
Documentation: Matplotlib Documentation

Deep Learning Theory and Emotion Recognition
Articles and papers on emotion recognition and YOLO:
Emotion Recognition from Facial Expressions: A Survey
YOLO Object Detection Papers and Resources

Resources for YOLO Training and Fine-Tuning
YOLO Training Guide: Ultralytics YOLOv5 Train Custom Data
Training on Custom Datasets (YouTube): Training YOLO Models - YouTube
FER Applications and Use Cases

## Issues and contribution
For this project the knowing issues are:
Class imbalance: Certain classes, such as disgust and sad, are under-represented in the dataset, leading to poor performance.
Subtle differences in emotions: Overlapping features between fear and neutral make classification challenging.
To contribute we will use:
Fork this repository and make a pull request.
Report issues or suggest improvements under the "Issues" section of this repository.
Add new datasets or propose alternative architectures for emotion recognition.


## Future work 
For this project i see a lot of things to upgrade in the future. 
First is the Class Balancing. We will need to increase the representation of underperforming classes using synthetic data or data augmentation techniques.
Next would be the Improved Architectures. We will experiment with other architectures such as EfficientNet or ResNet for emotion recognition.
Finally it will be the Real-world Deployment. Integrate the model into an application, such as a live emotion recognition system using webcam input.
