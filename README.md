# SamartMeathod_task1
This is first task for Samart Method 2022

Getting Started with ROS on Jetson Nano:

##Installation..

1: Set up Jetson Nano:

$ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu

$(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

2: To add new apt key:

$ sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

3: To update Debian packages index:

$ sudo apt update

4: To install the ROS Desktop package:

$ sudo apt install ros-melodic-desktop

5: To update .bashrc script:

$ echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc 

$ source ~/.bashrc

6: To install and initialize rosdep:

$ sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

$ sudo rosdep init 

$ rosdep update

##Configure a catkin workspace..

1:

$ sudo apt-get install cmake python-catkin-pkg python-empy python-nose python-setuptools libgtest-dev python-rosinstall python-rosinstall-generator python-wstool build-essential git

2: To create the catkin root and source folders:

$ mkdir -p ~/catkin_ws/src 

$ cd ~/catkin_ws/

3: Configure the catkin workspace:

$ catkin_make

4: update .bashrc script:

$ echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc

$ source ~/.bashrc

##Getting Started with ZED stereo camera on Jetson Nano..

1: get ZED running with ROS on Nano:

$ cd ~/catkin_ws/src

2: Clone the ZED ROS wrapper:

$ git clone https://github.com/stereolabs/zed-ros-wrapper.git

3: Check:

$ cd ~/catkin_ws

$ rosdep install --from-paths src --ignore-src -r -y

4: To Compile the ZED ROS wrapper:

$ catkin_make -DCMAKE_BUILD_TYPE=Release

$ roslaunch zed_display_rviz display_zed.launch

5: To ZED Mini:

$ roslaunch zed_display_rviz display_zedm.launch 















