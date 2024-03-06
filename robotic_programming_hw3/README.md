# Robotic Programming Homework 3

## Requirement
You need to be on Ubuntu version 20.04 with ROS already installed.

## Creating catkin workspace
In terminal
```bash
mkdir -p ~/catkin_ws/src
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
## Usage
To use the `my_turtle_controller` package, clone this repository then copy `my_turtle_controller` into the `src` folder of your catkin workspace.
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

## Running the Turtlesim
Open the terminal and run
```bash
roscore
rosrun turtlesim turtlesim_node
rosrun my_turtle_controller draw_circle.py
```
You should now see the turtle drawing a circle.

