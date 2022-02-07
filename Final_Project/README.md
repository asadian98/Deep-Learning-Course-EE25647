# Joint Object Detection and Depth Estimation

## Authors:
Amirhossein Asadian & Ahmadreza Rahimzare

## About the project:
In this project, first, we trained a model to *estimate depth* of any single image. The model we used is similar to [this project](https://github.com/siddinc/monocular_depth_estimation). It's based on papers [U-Net: Convolutional Networks for Biomedical Image Segmentation](https://arxiv.org/abs/1505.04597) and [High Quality Monocular Depth Estimation via Transfer Learning](https://arxiv.org/abs/1812.11941). Particularly, We used [NYU Depth Dataset V2](https://cs.nyu.edu/~silberman/datasets/nyu_depth_v2.html) for training.
<br> For *object detection*, we used network YOLOv3 which is a pretrained network on COCO dataset. It's fast and uses "darknet" as a deep neural network (Check [here](https://pjreddie.com/darknet/yolo/)).
<br> Finally, we joined two networks in series such that the depth estimation network is followed by the object detection network. One can choose objects in a 
certain depth range to be detected by the final network.

## Files:
<br>**Depth_Estimation.ipynb:** Creating, Training and saving the "depth estimation model".
<br> **YOLO_Object_Detection.ipynb:** Using YOLOv4 to detect objects in NYU Depth Dataset V2. 
<br> **YOLOv3_Object_Detection.ipynb:** Using YOLOv3 to detect objects in NYU Depth Dataset V2. 
<br> **Joint_Network.ipynb:** Depth Estimation followed by object detection (YOLOv3).
<br> **Report.pdf:** Detailed report of the whole project (in Farsi).

The trained "Depth Estimation Model" is also available [here](https://drive.google.com/drive/folders/1WwH5J9C5vVoIhgFO5PQyHodTGwUvEqZu?usp=sharing).

## Results:

Depth Estimation:

![depth_estimation](https://user-images.githubusercontent.com/94138466/152656702-6dd3f833-c0c6-4d53-9cef-d9161e83aaa8.png)

Object Detection Using YOLOv4:

![ObjectdetectedYOLOv4](https://user-images.githubusercontent.com/94138466/152656708-c5cde1aa-b7a6-431a-af74-942d9b821f20.png)

Object Detection Using YOLOv3:

![ObjectDetected](https://user-images.githubusercontent.com/94138466/152656704-0db9fd94-9aa6-4427-89d7-177d8045d5e4.png)


Joint Network Results (Depth Estimation + Object Detection Using YOLOv3):

![closerthan3m](https://user-images.githubusercontent.com/94138466/152656712-3918a385-9cf6-4515-85f4-2cb7745cd889.png)

![furtherthan2m](https://user-images.githubusercontent.com/94138466/152656714-6c117daa-ab89-440a-8d17-ec8ba8eaa18b.png)


