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
![image](https://github.com/user-attachments/assets/1693daf9-d378-4945-a1ae-93dfd69c9323)

## Installation and usage

## References and documentation

## Issues and contribution

## Future work 
For this project i see a lot of things to upgrade in the future. 
First is the Class Balancing. We will need to increase the representation of underperforming classes using synthetic data or data augmentation techniques.
Next would be the Improved Architectures. We will experiment with other architectures such as EfficientNet or ResNet for emotion recognition.
Finally it will be the Real-world Deployment. Integrate the model into an application, such as a live emotion recognition system using webcam input.
