# Task.2-ROS

# Step-by-Step Guide to Install ROS Noetic on Ubuntu 20.04 using VirtualBox
Step 1: Download and Install VirtualBox
Go to the VirtualBox download page and download the latest version for your operating system.
Install VirtualBox by following the instructions provided on the download page.
Step 2: Download Ubuntu 20.04.4
Download the Ubuntu 20.04.4 ISO from the official website.
Step 3: Create a Virtual Machine
Open VirtualBox and click on "New" to create a new virtual machine.
Name your virtual machine (e.g., "Ubuntu 20.04"), set the Type to "Linux," and the Version to "Ubuntu (64-bit)."
Allocate memory (RAM) to the virtual machine. A minimum of 2GB is recommended, but 4GB or more is preferred.
Create a virtual hard disk. The default settings are usually fine, but make sure to allocate enough space (at least 20GB).
Step 4: Install Ubuntu 20.04.4
Start the newly created virtual machine.
When prompted to "Select start-up disk," browse and select the downloaded Ubuntu 20.04.4 ISO file.
Follow the on-screen instructions to install Ubuntu. This includes selecting your language, keyboard layout, and creating a user account.
Step 5: Install ROS Noetic
Setup your sources.list
bash

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
Set up your keys
bash

sudo apt update
sudo apt install curl -y
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
Installation
First, make sure your Debian package index is up-to-date:

bash

sudo apt update
Install ROS Noetic Desktop-Full
bash

sudo apt install ros-noetic-desktop-full
Environment setup
bash

echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
Install dependencies for building packages
bash

sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
Initialize rosdep
bash

sudo apt install python3-rosdep
sudo rosdep init
rosdep update
Step 6: Start ROS
To start the ROS master, use the roscore command:

bash

roscore
With these steps, you will have ROS Noetic installed and running on Ubuntu 20.04 in a VirtualBox virtual machine. Let me know if you need any further assistance!
