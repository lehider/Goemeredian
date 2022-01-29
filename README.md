# Goemeredian
Setup your sources.list
-----------------------

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'


Set up your keys
----------------
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -


Installation
------------

sudo apt-get update

sudo apt-get install ros-kinetic-desktop-full

sudo apt-get install ros-kinetic-desktop

sudo apt-get install ros-kinetic-ros-base

Environment setup
-----------------
echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
source ~/.bashrc


Dependencies for building packages
-----------------------------------
sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential


Initialize rosdep


sudo apt install python-rosdep
rosdep update

Create ROS Space
----------------
 mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/
$ catkin_make


Hesai Lidar SDK Installation
----------------------------
$ sudo apt-get update
$ sudo apt-get install python-catkin-tools

$ mkdir -p rosworkspace/src
$ cd rosworkspace/src
$ git clone https://github.com/HesaiTechnology/HesaiLidar_General_ROS.git --recursive

 roslaunch hesai_lidar hesai_lidar.launch lidar_type:="PandarXTM" frame_id:="PandarXTM"


GNSS

rosdep install --from-paths src --ignore-src -r -y
