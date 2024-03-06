# Robotic Programming Homework 4

## Requirement
You need to be on Ubuntu version 20.04 with ROS already installed.

## Installation
You also need to install some additional packages:
```bash
sudo apt install ros-noetic-hector-gazebo-plugins
sudo apt install ros-noetic-velodyne-description
```

## Usage
To use this, you need to clone this repository then copy the content in `src` folder into the `src` folder of your catkin workspace.
Then build the workspace with `catkin_make` and source the new package:
```bash
cd ~/catkin_ws
catkin_make
```
```bash
source devel/setup.bash
```
OR
```bash
source devel/setup.sh
```

## Running the Simulation
Open the terminal and run
```bash
roscore
roslaunch smb_gazebo smb_gazebo.launch
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```
Now you should be able to control the robot with your keyboard.