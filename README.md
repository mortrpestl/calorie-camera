# Calorie Camera by @mortrpestl 
<p align="center">
  <a href="https://github.com/mortrpestl/calorie-camera/releases/download/v1/app-v1.apk">
    <img src="https://raw.githubusercontent.com/mortrpestl/calorie-camera/main/app_icons/icon.png" alt="Icon" />
  </a>
</p>

My own take on estimating calories based on an object detection app based on YOLOv8. Some software used include Android Studio (with Kotlin), Google Colab, and Python. [Dataset](https://universe.roboflow.com/food-1b74y/food-recognition-challenge/dataset/2/download) obtained from Roboflow. More info on the bottom for helpful repositories.

# Documentation
## Example Predictions of Model

The model used was trained with 100 epochs (I later adjusted the epochs to 50 for easier use on low-end devices, but this was not used for in the final model). There are a total of 22 classes based on the [dataset](https://universe.roboflow.com/food-1b74y/food-recognition-challenge/dataset/2/download) used. These classes can be found on the [data.yaml](https://github.com/mortrpestl/calorie-camera/edit/main/data.yaml) file. Below are some of the predictions of the TFlite model.

<p align="center">
  <img src="https://raw.githubusercontent.com/mortrpestl/calorie-camera/main/docu/predict1.jpg" alt="Predict1" width="22%" />
  &nbsp;&nbsp;
  <img src="https://raw.githubusercontent.com/mortrpestl/calorie-camera/main/docu/predict2.jpg" alt="Predict2" width="22%" />
  &nbsp;&nbsp;
  <img src="https://raw.githubusercontent.com/mortrpestl/calorie-camera/main/docu/predict3.jpg" alt="Predict3" width="22%" />
  &nbsp;&nbsp;
  <img src="https://raw.githubusercontent.com/mortrpestl/calorie-camera/main/docu/predict4.jpg" alt="Predict4" width="22%" />
</p>

## App Usage (alpha)

You may download the file [here](https://github.com/mortrpestl/calorie-camera/releases/tag/v1) and try it out for yourself.

<p align="center">
  <img src="https://raw.githubusercontent.com/mortrpestl/calorie-camera/main/docu/banana.jpg" alt="Banana" width="45%" />
  &nbsp;&nbsp;
  <img src="https://raw.githubusercontent.com/mortrpestl/calorie-camera/main/docu/veggies.jpg" alt="Veggies" width="45%" />
</p>

## Recommendations
- Expand the dataset (at least 500 images per category).
- Use a faster device to model (to train 100 epochs took my computer 20 hours).

# Software, Dependencies, Paradigms Used
## Software
- [Python](https://www.python.org/)
- [Android Studio](https://developer.android.com/studio)
    - [Kotlin](https://kotlinlang.org/)
- [LiteRT (formerly TensorFlow Lite)](https://ai.google.dev/edge/litert)

## Paradigms
- [YOLOv8](https://github.com/ultralytics/yolov8)

## Dependencies
- [Ultralytics](https://github.com/ultralytics)
- Other Python modules
  
## Repositories
- [Food Recognition Dataset](https://universe.roboflow.com/food-1b74y/food-recognition-challenge/dataset/2/download)
- [Aarohi Singla's Object Detection paradigm](https://github.com/AarohiSingla/Object-Detection-Android-App)
- [Surendra Maran's Android implementation of TFlite](https://github.com/surendramaran/YOLOv8-TfLite-Object-Detector)

