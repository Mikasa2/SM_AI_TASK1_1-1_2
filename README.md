# SM_TASK1_DownloadROSinUbunto
Download ROS on ubunto 22.04 
#Write in terminal 

#Set locale

1. locale  # check for UTF-8

2. sudo apt update && sudo apt install locales

3. sudo locale-gen en_US en_US.UTF-8

4. sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8

5. export LANG=en_US.UTF-8

6. locale  # to verify settings



#Setup Sources


7. sudo apt install software-properties-common

8. sudo add-apt-repository universe

9. sudo apt update && sudo apt install curl gnupg lsb-release

10. sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg

11. echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

#Install ROS 2 packages

12. sudo apt update

13. sudo apt upgrade

14. sudo apt install ros-humble-desktop

15. sudo apt install ros-humble-ros-base


#Environment setup


16. source /opt/ros/humble/setup.bash
