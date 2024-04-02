# Robotic Programming Homework 4

## Requirement
You need to be on Ubuntu version 20.04 with ROS already installed.

## Usage
To use this, you need to clone this repository then copy the `two_link_description` folder into the `src` folder of your catkin workspace.
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
roslaunch two_link_description gazebo.launch
```
Now the robot simulation should start and you should be able to see the robot.
