## Object detection exercise

This exercise attempts to demonstrate if a Convolutional Neural Network (CNN) is able to detect objects within a picture. For a simple example, two classes will be considered: Cars and pedestrians.

40 images were downloaded from the internet, containing cars and/or pedestrians (in the form of persons). The images were then manually labelled using labelimg software, and exported in YOLO format.

Train, validation and test folders were then created, in compliance with Yolov5 format requirements. Yolov5 library is then downloaded onto the local environment. A YAML file to indicate the path to the train, validation and test folders and the binary classes is also prepared. Transfer learning with training is then applied. Last step is to apply object detection over the test images.

### Training:

- First 10 layers of Yolov5 (the backbone) was used for transfer learning
- Train-val split: 32 train, 8 validation

### Results:

1. Training results after 50 epochs, with confidence at 0.4 and IOU at 0.5: https://github.com/chanhanxiang/yolov5_run2/tree/master/from_yolo/runs/train/exp3

2. Detection of test images (3 images): https://github.com/chanhanxiang/yolov5_run2/tree/master/from_yolo/runs/detect/exp3

## Note:

Files from yolov5 are not included in package, please download seperately when running ipynb
