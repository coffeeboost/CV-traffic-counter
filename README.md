# CV-traffic-counter

## About this project
The goal is to count the number of passing cas through an intersection. To achieve this, I used pytorch, opencv, numpy, and SORT object tracker.


## Object design
Logically separate code to switch parts out easier.
- Transform
- Util
- Counter
- Model

## Program flow
- load video with torchvision.io
- process each frame to fit COCO normalisation requirements
- crop image to area of interest
- load pre-trained COCO trained model and set to eval mode
- get bounding boxes predictions
- pass bbox to SORT to track object
- plot bbox to image
- count number of unique ID from SORT

## Limitations
- video frames must fit in colab RAM space, 1GB video is too big.
- COCO requirements, min size of 224x224 px
- Horrible object detection?

## How to run
1. cells 1 to 3 set up the environment
2. 4th cell and below are normal
