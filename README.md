# Gesture Classification on Human Skeleton Gesture recognition

The video data was collected and processed using [MediaPipe](https://google.github.io/mediapipe/) $-$ a machine learning solution for high-fidelity body pose tracking, inferring `33` 3D landmarks and background segmentation mask on the whole body from RGB video frames utilizing our research for human skeleton gesture recognition.

## Dataset Description

### Samples
- 7420 4D samples
- 120 times on three-coordinates 
- 67 joints (25 body, 21 leftHnad 21 rightHand)

### Labels
`53 labesls (0 to 52) 16 for leftHand, 16 for rightHand, 19 for bothHands, 2 for head`

### Labels set
`righthand = [2,5,8,18,20,23,26,29,31,33,35,37,39,41,44,52]` \
`lefthand = [1,4,7,9,17,19,22,25,28,30,32,34,36,38,40,43]` \
`bothhand = [0,3,6,10,11,12,13,14,15,16,21,24,27,42,45,46,47,48,49,50,51]`

- 21 joints for each left and right hand fingers, 42 in-total.
- 25 joints for the body without legs.

## Classification Tasks:

### For our multi-classes classification tasks, the classification algorithms are applied primarily on three classes classification ie. Left, right, both. Next, the data is divided into lefthand, righthand, & bothhand datasets, and the classification model is trained on lefthand (16) classes, righthand (16) classes, bothhand (19) classes.  

## For training model , the  supervised learning methods is implemented, Naive-Bayes-Gaussian Method & Linear-Regression method. 

The best performance was by Linear Regression (LR) classification modal on whole dataset for three classes, the accuracy achieved after 500 iteration was 99.78%. 
For multi-classes classification problem, the accuracy decreased marginally. For Naive Bayes Gaussian (NBG), best accuracy was achieved on reduced dimentionality data using t-SNE approach. The table below sumarize the achieved results: 


| Model | Classes | Dataset | Accuracy % | 
|--------|----------|---------|----------|
| LR | 3 | whole | 99.78 |
| LR | 16 | lefthand | 86.93 |
| LR | 16 | righthand | 82.33 | 
| LR | 19 | bothhand | 93.85 |
| NBG | 3 | whole | 91.28 | 
| NBG | 3 | t-SNE | 96.80 | 

\
For more information or discussion, feel free to write me on [Telegram](https://t.me/tomarp) or [email](mailto:p.tomar@outlook.de?subject=[GitHub]). \
Please feel free to leave a comment or any suggestions. Happy learning. 
