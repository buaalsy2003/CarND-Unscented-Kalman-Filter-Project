# Project 7 - Unscented Kalman Filter Project
Self-Driving Car Engineer Nanodegree Program

Implemented a C++ Unscented Kalman Filter program to fusion Lidar and Radar sensor data input. Lidar data can accurately define an object's location. Radar data provides not just location but also speed data that can be used to track an object's velocity relative to the sensor. 

---

## Dependencies

* cmake >= v3.5
* make >= v4.1
* gcc/g++ >= v5.4

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: 
   `./UnscentedKF ../data/obj_pose-laser-radar-synthetic-input.txt output.txt` 
   and
   `./UnscentedKF ../data/sample-laser-radar-measurement-data-1.txt output2.txt`

## Results

Root Mean Square Error (RMSE) Accuracy were calculated for the dataset:
obj_pose-laser-radar-synthetic-input.txt
* px        0.0647819
* py        0.0864608
* vx        0.360615
* vy        0.270453


I also compared this Unscented Kalman Filter with previous project using Extended Kalman Filter. 

UKF project result for sample-laser-radar-measurement-data-1.txt:
* px	       0.0350618
* py	       0.0418754
* vx	       0.524488
* vy	       0.48888

EKF project result for sample-laser-radar-measurement-data-1.txt:
* px	       0.0620209
* py	       0.057777
* vx	       0.521125
* vy	       0.53581

It shows that UKF is more accurate regarding non-linear input. 

## Future Work

I'd like to generate your own radar and lidar data, using the
[utilities repo](https://github.com/udacity/CarND-Mercedes-SF-Utilities) for
Matlab scripts that can generate additional data.
