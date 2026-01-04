# Project: Vision based Tracking
The goal of this project is to used to track objects in a video stream and plot their trajectory as 2D/3D graph

The goal will be achieved in multiple steps. 

The first step will be to identify objects from an image. 

Here, objects will be people or other named objects like the license plate, animals. 

## Object identification from an image. 
YOLO v8 from Ultralytics will be used to identify the objects of an image. The whole project is built in a Google Colab environment. The algorithm reads the images from source folder and if an object is detected, this object is named and labelled and a named images is stored in the destination folder. 

