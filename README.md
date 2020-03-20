# High Power Rocketry tracker with Python

## Description
Rocket launches are of great interest and many efforts have been made to automate the capturing process of close-up the take offs on camera. The capturing automation can be achieved by either object tracking, frame-by-frame object detection or combinations, depending on the problem limitations.
The main aim of this project is to offer a robust detector/tracker, capable to operate at almost real time with limited hardware resources, for the automated recording of the rocket launches. The algorithm will be combined with the single-board computer Raspberry which will be moving the camera. The hardware set-up of the camera motion is not part of this projects.
Implementation plan
The project consists of two components:

The rocket detection model.
The core component of most modern trackers is a discriminative classifier, tasked with distinguishing between the target and the surrounding environment. To cope with natural image changes, this classifier is typically trained with translated and scaled sample patches.
A model will be created using TensorFlow and Keras on Python3. It will be trained on multiple images containing rockets of different sizes, colors and orientations and it will output a bounding box when a rocket is detected.
The rocket tracking algorithm.
Once the object is identified, the tracking algorithm is applied. That way the information of past frames is considered and position of the object is predicted, allowing us to follow the flight trajectory. In case that the track algorithm fails (i.e. cannot track correctly the object), we rerun the detection model.
The tracking algorithm will be running on the Raspberry PI, which will be moving the camera in order to track and record the rocket the whole time. The OpenCV library will be used.

## Features

### Todo

- [x] Setup yolov3
- [x] Convert dataset to yolov3 format. Check [this](C:\Users\Helios\Desktop\Google Image Downloader + Rocket Dataset\converter-scripts) out to know how to do that.
- [x] Train the yolov3 model on custom dataset
- [x] Upload weights and share here via Mega or GDrive
- [x] Added webcam mode with realtime rocket detection
- [x] Added video file mode with realtime object detection
- [x] Upload demo video online. Link coming soon.

## How to use

- `git clone https://github.com/sunn-e/OpenCV-Yolov3-CPU/`
- `cd OpenCV-Yolov3-CPU`
- download weights and configuration file from [here](https://pjreddie.com/darknet/yolo/)
- download coco.names from [here](https://github.com/pjreddie/darknet/blob/master/data/coco.names)
- run the main notebook using jupiter notebook
- Give input/objects when prompt opens.
- Custom folder name is supported, may have to change script a little
- Wait for pictres to get displayed
- Open "TinyYolov3-Prototype-custom-rocket.ipynb" in 

## Contribute

Feel free to fork it and create your own versions. Make sure you have installed all the dependencies

## Getting Started

simply clone the repository to acquire the dataset.

## Dependencies

### Prerequisites

- Python 3.x+
- OpenCV 2
- numpy
- jupyter notebook

#### specially for opencv

```
pip install opencv-contrib-python
```

#### For weights

- You may copy paste the image folders to your intended location or simply copy past the path to out machine learning/deep learning model script.


## Built With

- [Python 3.x+](https://www.python.org/download/releases/3.0/)
- [opencv](https://opencv.org/)
- [Yolo v3](https://pjreddie.com/darknet/yolo/)

## Contributing

Clone and see if you find anything to improve upon. You can also create issues using that tiny issue button.

## Versioning

Git

## Dataset

The dataset(coming soon) is inside data folder with image folder names corresponding the search term used to download those images.
Meanwhile check [this](https://github.com/sunn-e/Google-Image-Downloader-Rocket-Dataset) out!

## Notice

The images(if any), videos have been provided for educational purpose and are owned by their respective owners.

## Authors

* **Sunny Dhoke** - *Initial work* - [sunn-e](https://github.com/sunn-e)

## License

[LICENSE.md](LICENSE.md) file for details
