# Estimate Tilt Angle of Phone using Gyroscope and Accelerometer

This is an implementation of estimating and trackiing the tilt angle of a moving or static IOS phone with the data from gyroscope and accelerometer (IMU on phone). The code is adapted from github repository from [justin chan](https://github.com/justinklchan/imu_iphone)

## What is it
This project leverages the gyroscope and accelerometer already embedded in most commodity phone devices to estimate the tilt angle of phone when it is moving. The tilt angle is defined as the angle ρ between the gravitational vector measured by the accelerometer and the initial orientation with the gravitational field pointing downwards along the z-axis. 
<img width="497" alt="Screen Shot 2022-06-01 at 1 59 57 PM" src="https://user-images.githubusercontent.com/46943965/171500709-5eb50fd9-6cc2-4431-891c-5483a58a3ff5.png">

To do this, we generate an inaudible tone, which gets frequency-shifted when it reflects off moving objects like the hand. We measure this shift with the microphone to infer various gestures.

## How to use

To test this program, you should firstly disable in the microphone settings, the echo cancelation and the noise reduction. Control Panel -> Sound -> Recording -> Microphone Array -> Propertoes -> Advanced -> Disable Audio Enhancements

Then run
```
python main.py
```

## Demo
Demo of running code on iphone in real time:

https://user-images.githubusercontent.com/46943965/170893234-9c12533f-29b1-4c13-a56b-96caf32e4c79.mp4

