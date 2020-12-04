# Simple_Arm

This Project explain pub-sub architecture in ROS.

#### Once the `simple_arm` package has been built, you can launch the simulation environment using
```sh
$ roslaunch simple_arm robot_spawn.launch
```

#### Interact with the arm using the safe_move service
Open a new terminal and type the following:
```sh
$ cd /home/workspace/catkin_ws/
$ source devel/setup.bash
$ rosservice call /arm_mover/safe_move "joint_1: 0.0 joint_2: 0.0"
```

## How to view image stream from the camera?
Camera image stream is published to the following topic:
```
/rgb_camera/image_raw
```

This stream can be viewed by following command in separate terminal:
```sh
$ rosrun image_view image_view image:=/rgb_camera/image_raw
```
