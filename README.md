# CV-traffic-counter
# WIP

## About this project
The goal is to count the number of passing cas through an intersection. To achieve this, I used pytorch, opencv, numpy, and SORT object tracker.

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

## How to run
1. run the first cell to install extra dependencies
2. restart runtime environment
3. continue after the first cell like normal
