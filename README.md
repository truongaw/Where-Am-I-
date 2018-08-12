# Where-Am-I-
Robotic Mapping Project with SLAM implementation

The project goal was to implement the adaptive monte carlo localization (amcl) algorithm in simulation programs, Gazebo
and RViz. The amcl algorithm uses particles to predict the robot’s pose and orientation. Adaptive monte carlo algorthm differs from the
basic monte carlo algorithm by adapting the number of particle prediction for each forecast. The project also reviewed URDF code for
the setup and simulation of a robot. The robot used in this project has a chassis with two cylindrical wheels and two caster wheels for
stability. The robot is placed in a maze and the goal of the project is to use amcl to accurately navigate the maze to the goal
destination. Several amcl parameters were tuned in the algorithm for precise particle forecasting. The project is complete when the
robot reaches the goal destination with an accurate pose array. A new robot designed with new amcl parameters was created to
compare the amcl parameters with the initial robot design.

Index Terms—Robot, IEEEtran, Udacity, LATEX, Localization


# Where Am I?

In this project, you will learn to utilize ROS packages to accurately localize a mobile robot inside a provided map in the Gazebo and RViz simulation environments.

Over the course of the project, as part of the Robotics Software Engineer Nanodegree, you will learn about several aspects of robotics with a focus on ROS, including -

- Building a mobile robot for simulated tasks.

- Creating a ROS package that launches a custom r-obot model in a Gazebo world and utilizes packages like AMCL and the Navigation Stack.

- Exploring, adding, and tuning specific parameters corresponding to each package to achieve the best possible localization results.

## Installation Instructions

The project can be complete in the provided Workspace in the Classroom. Alternatively, it can be completed on an Ubuntu System with ROS Kinetic installed on it. Some specific ROS packages might be required in order to complete the project -


``` bash
$ sudo apt-get install ros-kinetic-navigation
$ sudo apt-get install ros-kinetic-map-server
$ sudo apt-get install ros-kinetic-move-base
$ rospack profile
$ sudo apt-get install ros-kinetic-amcl
```

**Note:** We won't be able to provide support for native ROS installations, but you can post in the #ros channel in the ND Slack to start discussions with your fellow students if you face any issues.

Once all the packages are installed, clone the repository on your system and rename the project folder to `udacity_bot`. However, it is recommended that you follow the Classroom instructions on working through the project instead of cloning the repo.


## Run the Project

After completing the project, you can launch it by running the following commands first -

```bash
$ cd ~/catkin_ws
$ catkin_make
$ source devel/setup.bash
```

And then run the following in *separate* terminals -

``` bash
$ roslaunch udacity_bot udacity_bot
$ roslaunch udacity_bot amcl
$ rosrun udacity_bot navigation goal
```
