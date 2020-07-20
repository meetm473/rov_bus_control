# rov_bus_control
A ROS package containing files required to control the underwater ROV Bus in Gazebo. The [rov_bus][1] package is must for the nodes of this package to function properly.

### Commands
To control the ROV using keyboard keys (without camera output)
```
roslaunch rov_control rover_controller.launch
```
To control the ROV using keyboard keys (with camera output)
```
roslaunch rov_control rover_controller.launch use_rviz:=true
```
> In the terminal, press *h* to display help for keyboard control.

[1]:https://github.com/meetm473/rov_bus
