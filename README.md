ua_ros_p3dx
===========

A ROS/Gazebo Pioneer 3DX model.

To install:
```
cd <catkin_ws>/src
git clone https://github.com/miguelvidex/PioneerModel.git
catkin build
```
To run the gazebo environment with pioneer3dx in gazebo:

(terimnal 1)
```
roscore
```
(terminal 2)   --  you can change the world file adding this: world_name:='---world_desired---'
```
roslaunch p3dx_gazebo gazebo.launch 
```
(terminal 3)   -- optional --  if you want to see the robot in rviz 
```
roslaunch p3dx_description rviz.launch 
```
To see the urdf model of robot with camera:
(terminal 1)
```
roslaunch p3dx_description test_urdf.launch
```

To teleoperate the robot by the terminal:
Install a package
```
sudo apt-get install ros-kinetic-teleop-twist-keyboard
```
Run the node to teleoperate the robot, publishing on the topic /cmd_vel
```
rosrun teleop_twist_keyboard teleop_twist_keyboard.py cmd_vel:=/cmd_vel
```
