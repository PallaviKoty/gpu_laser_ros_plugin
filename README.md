# gpu_laser_ros_plugin

This is the ROS plugin for gpu_laser sensor

Steps to use this plugin:
1. Clone `common_msgs` for melodic and compile it using the command
```
catkin_make --only-pkg-with-deps common_msgs
```
2. `source devel/setup.bash`
3. Compile the `gazebo_laser_plugin` package using the command,
```
catkin_make --only-pkg-with-deps gazebo_laser_plugin
```
4. `source devel/setup.bash`
5. Launch the launch file using the command,
```
roslaunch gazebo_laser_plugin launch_gpu_ros.launch
```
6. After Step 5, we can see gazebo is up with the laser and few obstacles(but cannot see the laser signals yet though, need to check)
7. Launch RViz in another terminal using the command,
```
cd <path_to_gpu_laser_plugin_ws>
source devel/setup.bash
rviz
```
8. Add the `laser_scan` topic and change the frame to `world` or `laser_sensor` on RViz. You can now see the laser scans on RViz
9. We can also get the laser scan data using
```
rostopic echo /laser_scan
```
