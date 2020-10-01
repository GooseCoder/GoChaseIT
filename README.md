
# Go Chase It!

The Go Chase It project is an autonomous vehicle simulation, with two main components: A wheeled robot and a ball chaser. In the simulation the wheeled robot follows the ball until reaches it.

## Project Structure

```
.
├── ball_chaser
│   ├── CMakeLists.txt
│   ├── include
│   │   └── ball_chaser
│   ├── launch
│   │   └── ball_chaser.launch
│   ├── package.xml
│   ├── src
│   │   ├── drive_bot.cpp
│   │   └── process_image.cpp
│   └── srv
│       └── DriveToTarget.srv
└── my_robot
    ├── CMakeLists.txt
    ├── launch
    │   ├── robot_description.launch
    │   └── world.launch
    ├── meshes
    │   └── hokuyo.dae
    ├── package.xml
    ├── urdf
    │   ├── my_robot.gazebo
    │   └── my_robot.xacro
    └── worlds
        └── HomeFirstFloor.world
```

## How to use the project

First launch the main robot component.

```
$ cd /home/workspace/catkin_ws/
$ source devel/setup.bash
$ roslaunch my_robot world.launch
```

Then launch the ball chaser.

```
$ cd /home/workspace/catkin_ws/
$ source devel/setup.bash
$ roslaunch ball_chaser ball_chaser.launch
```

Once gazebo starts you can move the white ball there and the robot will follow it, if it's range of the frontal camera.
