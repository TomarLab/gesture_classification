# Gesture Classification on Human Skeleton and Action

The video data was collected and processed using [Mediapipe](https://google.github.io/mediapipe/): a machine learning solution for high-fidelity body pose tracking, inferring 33 three-D landmarks and background segmentation mask on the whole body from RGB video frames utilizing our BlazePose research that also powers the ML Kit Pose Detection API.

## Dataset Description

### Samples
- 7420 4d_full,  2798 4d_oneHand
- 120 times, x,y,z co-ordinates
- 67 joints (25 body, 21 leftHnad 21 rightHand)

### Labels
##### 53 labesls (0 to 52) == 16 for leftHand, 16 for rightHand, 19 for bothHands, 2 for head

### Labels set
- righthand = [2,5,8,18,20,23,26,29,31,33,35,37,39,41,44,52]
- lefthand = [1,4,7,9,17,19,22,25,28,30,32,34,36,38,40,43]
- bothhand = [0,3,6,10,11,12,13,14,15,16,21,24,27,42,45,46,47,48,49,50,51]

- 21 + 21 for the fingers for left and right hand
- 25 for the body without legs

## Classification Tasks:

### For classification classes tasks, the classification algorithms are applied primarily on three classes classification ie. Left, right, both. Next, the data is divided into lefthand, righthand, & bothhand datasets, and the classification model is trained on lefthand (16) classes, righthand (16) classes, bothhand (19) classes.  

## For training model , the  supervised learning methods is implemented, Naive-Bayes-Gaussian Method & Linear-Regression method. 

The best performance was by Linear Regression classification modal on whole dataset for three classes. The accuracy can be checked in the linear-regression implementation. 
