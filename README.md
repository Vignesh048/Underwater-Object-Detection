# Underwater-Object-Detection
### Master Thesis Project

The Brackish dataset, an underwater dataset with 6 different categories of videos is taken and images are extracted and divided into train test and validation splits. A pretrained model of Faster RCNN with ResNeXT as RPN is taken from detectron2 and fine tuned on the brackish dataset for limited number of epochs considering computation power available. The results are evaluated on the test set and different Average Precision Values are noted.
Using the results, in this project we conclude that pretraining on ordinary non - underwater dataset does not help on Underwater Object Detection Task.


![image (9)](https://user-images.githubusercontent.com/94463366/190477749-0dc291f7-c22e-43f4-8089-b8183244d7b6.jpg)

The pretrained Faster RCNN model with weights obtained from COCO Dataset is used in the project. The model is fine tuned with Brackish Dataset and evaluated on test data and the results are noted. The batch size taken is 64 frames for each pass. Out of 14518 frames, 11603 frames are used for training and 1467 frames are used for validation and 1468 frames used for test. The model is finetuned for 750 epochs. The model is evaluated for each 250 iterations and Average Precision scores are calculated for 6 different classes and different scales. The model weights are updated without freezing the bottom layers.The detectron2 library is used for loading and training the Faster RCNN Model.


