# Vehicle Speed Calculation using YOLOV and StrongSORT

## Introduction
This repository contains the experimental source code for a research paper titled "Computer Vision Application in Management of Vehicle Speed in Factory Area". For more details about the methodology and model, please refer to the [journal article](https://ieeexplore.ieee.org/abstract/document/10473636).

This project focuses on creating a model for estimating vehicle speeds based on video footage. The **YOLOV** model is employed to **detect vehicles**, while **StrongSORT** is used for **vehicle tracking**. The speed calculation is carried out using the formula **v = s/t**, where **v** represents velocity, **s** denotes distance, and **t** stands for time.
## Method
This section outlines our proposed research methodology. Data directly collected from cameras is passed through an object detection model, followed by object tracking. The results of the object tracking process are the coordinates of the positions that vehicles have moved through. These coordinates over time are used to calculate the average vehicle speed over time. The system is integrated to send direct messages via Telegram if the system detects vehicles exceeding the allowed speed limit.
<div style="text-align:center">
  <img src="Flow_method.png" alt="Method">
</div>

## Camera Calibration
This section describes the process of calibrating the data before use for calculations. All data needs to undergo computation and calibration to determine the parameters between pixel image and real-world distance.

![Calibration](Cablibration_method.png)

## Result Demo

This is a real-time demonstration video of the entire system's operation, including vehicle detection, vehicle tracking, speed measurement, database storage, and sending via Telegram.

![Demo](carspeed.gif)

[Download Demo Video (carspeed.mp4)](carspeed.mp4)

## Result Comparison
I utilized various methods to evaluate the results based on ground truth to determine the best calibration solution for each camera.
![Sample Image 1](1.png)
![Sample Image 2](2.png)
![Sample Image 3](3.png)
