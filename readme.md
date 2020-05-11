# How to use

This repo is to calibrate DDL Vimba camera and Ouster lidar based on 3D-to-3D correspondence method, and also to project 2D color info onto point clouds.


Notes:

- Check in the [catkin_ws_camLidarCalib repo](https://github.com/ntthuy11/catkin_ws_camLidarCalib/tree/master/src/cam_lidar_calib/calibration_data) for calibration data.

- When the lidar result shows up (i.e. white points on black background to represent for edge points of the Aruco marker boards), to select them for the algorithm, do

    1. mouse left-click on the virtual rectangle surrounding one edge,

    2. at every one mouse click, press Enter (line cofficients will show up in the terminal),

    3. once 4 corner points of the virtual rectangle are collected, move on to the other edges until it is done for one Aruco marker board (i.e. we need totally 4 x 4 mouse clicks plus 4 x 4 Enter key presses),

    4. do the same for other marker boards.

- Make sure the `initial rotation` is defined correctly in `config_file.txt`. For example, `-1.57 1.57 3.14` (for rx, ry, and rz) when

    - `rx = -1.57`: the camera is front of the lidar (x axis)

    - `ry = 1.57`: the camera is in the same y axis with the lidar

    - `rz = 3.14`: the camera is at the same rotation z with the lidar. If `rz = 0`, the lidar points might be projected up-side-down on the image


# Packages

[outer_example](https://github.com/ouster-lidar/ouster_example) was copied into this repo at the version
```
Latest commit 68ad03c on May 13, 2019
```

[lidar_camera_calibration](https://github.com/ankitdhall/lidar_camera_calibration) was copied into this repo at the version
```
Latest commit 8566e9b 19 days ago
(the day when this file is pushed is Apr 26, 2020)

```
