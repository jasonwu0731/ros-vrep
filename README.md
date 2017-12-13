# ROS + VREP

### ROS install and catkin
1. Install catkin: http://wiki.ros.org/catkin
2. Install ROS: http://wiki.ros.org/ROS/Installation
3. Configure and create catkin workspace
```
$ echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
$ source ~/.bashrc
$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/
$ catkin_make
$ echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
$ source ~/.bashrc
```
4. Install the needed ros packages
```
#install hector slam
$ sudo apt install ros kinetic hector slam
#install key teleop
$ sudo apt install ros kinetic key teleop
```

### Install V-REP
1. Dowload V-REP: http://www.coppeliarobotics.com/downloads.html
```
$ cp V-REP_PRO_EDU_V3_4_0_Linux.tar.gz ~
$ tar -zvxf ~/V-REP_PRO_EDU_V3_4_0_Linux.tar.gz
$ mkdir ~/V-REP
$ mv ~/V-REP_PRO_EDU_V3_4_0_Linux ~/V-REP
```

### Load RosInterface and Some Packages
* Copy everything in this repo *except* `README.md env.ttt hector.launch picture/ ` to `~/catkin_ws/src/`
```
$ cd ~/catkin_ws/
$ catkin_make
$ source ~/.bashrc
```
* Copy libv_repExtRosInterface.so
```
$ cd catkin_ws/devel/lib
$ cp libv_repExtRosInterface.so  ~/V-REP
```
