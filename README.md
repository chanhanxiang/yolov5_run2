## Object detection exercise

This exercise attempts to demonstrate if a Convolutional Neural Network (CNN) is able to detect objects within a picture. For a simple example, two classes will be considered: Cars and pedestrians.

40 images were downloaded from the internet, containing cars and/or pedestrians (in the form of persons). The images were then manually labelled using labelimg software, and exported in YOLO format.

Train, validation and test folders were then created, in compliance with Yolov5 format requirements. Yolov5 library is then downloaded onto the local environment. A YAML file to indicate the path to the train, validation and test folders and the binary classes is also prepared. Transfer learning with training is then applied. Last step is to apply object detection over the test images.

### Training:

- First 10 layers of Yolov5 (the backbone) was used for transfer learning
- Train-val split: 32 train, 8 validation

### Results:

Best performing training and test results are outlined below:

<h5>1. Training results after 50 epochs, with confidence at 0.4 and IOU at 0.5:</h5>

<img src="https://github.com/chanhanxiang/yolov5_run2/assets/107524953/16b3f121-eda7-421f-af4c-a245f61bcbf1" width=40% height=40%>

From the Confusion matrix plot, pedestrians have the best true positive prediction rate of 0.93, while for cars it is more modest with a score of 0.69.

More information at: https://github.com/chanhanxiang/yolov5_run2/tree/master/from_yolo/runs/train/exp3



<h5>2. Detection of test images (3 images):</h5>

<img src="https://github.com/chanhanxiang/yolov5_run2/assets/107524953/3098c052-7751-4453-accd-78a7abc51c35" width=40% height=40%>

Person is detected with high confidence, but car is barely detected at 0.43.

<img src="https://github.com/chanhanxiang/yolov5_run2/assets/107524953/d34ec331-2e23-49a7-9a12-195c635156be" width=40% height=40%>

Jaywalker and car at mid-distance able to be detected, cars further down the road can be detected.

<img src="https://github.com/chanhanxiang/yolov5_run2/assets/107524953/0bda7d7d-05cf-481d-ada4-c338116093d8" width=40% height=40%>

Jogger is detected well, parked cars are also detected.


More information at: https://github.com/chanhanxiang/yolov5_run2/tree/master/from_yolo/runs/detect/exp3

### Note:

Files from yolov5 are not included in package, please download seperately when running ipynb
