# Emotion-detection
# Description:
This Emotion detection project is part of a bigger project which is building an assistant for visually impaired people that can make their lives easier by using image captioning (to describe the scene abstractly) , object detection(to tell the user the place of a specific object they are looking for) , face recognition(to tell the user who is standing in front of them), and emotion detection techniques (to tell the user how is the person in front of them is feeling from the way they look because this part of communication is always missing for the blind people)  then all these outputs are converted to speech as a feedback to the user.

# Model Architecture:
For emotion prediction VGG16 model was tried but it didn't give any promising results, and i couldn't try large transfer learning networks like Resnet50 or inception due to the limited resources so i decided to build a model from scratch with the following architecture:

![architecture](https://user-images.githubusercontent.com/103740764/185250305-a58ed432-efc6-409f-aa2c-d3f821623056.png)
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
For inference first we pass the input streaming video frames to haar cascade to detect the face, crop it and send it to the model to perform the prediction and draw a bounding box on the face with the emotion written above it.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Dataset:
 I used FER-2013 dataset which consists of 48x48 pixel 35887 grayscale images of faces. The faces have been automatically registered so that the face is more or less centred and occupies about the same amount of space in each image.
Face based on the emotion shown in the facial expression into one of seven categories (Angry, Disgust, Fear, Happy, Sad, Surprise, and Neutral). 
Dataset link:
https://www.kaggle.com/datasets/deadskull7/fer2013
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Results:
The obtained validation accuracy after training on 120 epochs was 0.66 which is the quite normal for this field of study as it is still under research, and based on research papers this was highest accuracy obtained in this field of study without using transfer learning
![Accuracy_emotion](https://user-images.githubusercontent.com/103740764/185254429-003f2284-cb58-4263-a90d-09e324106272.png)
![Loss_emotion](https://user-images.githubusercontent.com/103740764/185254436-57aa3761-2c56-4d66-b018-41eb93d7f5f7.png)
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# User guide:
