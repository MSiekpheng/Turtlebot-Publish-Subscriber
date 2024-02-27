# Introduction
This repository provides instructions on how to run the Turtlesim simulation and make it draw a circle.

## Requirement
You need to be on Ubuntu version 20.04 with ROS already installed.

## Creating catkin workspace
In terminal
```bash
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws
catkin_make
source devel/setup.bash
```
## Creating a new ROS package
In terminal
```bash
cd ~/catkin_ws/src
catkin_create_pkg my_turtle_controller rospy turtlesim geometry_msgs
cd my_turtle_controller
mkdir scripts
```
## Creating a Python script to make the Turtlesim draw a circle
In terminal
```bash
cd ~/catkin_ws/src/my_turtle_controller/scripts
touch draw_circle.py
chmod +x draw_circle.py
```
Open the Python file in any IDE of choice then paste in the codes below.
```python
#!/usr/bin/env python3
import rospy
from geometry_msgs.msg import Twist

if __name__ == '__main__':
    rospy.init_node("draw_circle")
    rospy.loginfo("Node has been started.")

    pub = rospy.Publisher("/turtle1/cmd_vel", Twist, queue_size=10)

    rate = rospy.Rate(2)

    while not rospy.is_shutdown():
        msg = Twist()
        msg.linear.x = 2.0
        msg.angular.z = 1.0
        pub.publish(msg)
        rate.sleep()
```
Save the file then in the terminal
```bash
cd ~/catkin_ws
catkin_make
source devel/setup.bash
```
To make sure that `rosrun` can find the new package
## Running the Turtlesim
Open the terminal and run
```bash
roscore
```
In another terminal
```bash
rosrun turtlesim turtlesim_node
```

In the third terminal
```bash
rosrun my_turtle_controller draw_circle.py
```
You should now see the turtle drawing a circle.

