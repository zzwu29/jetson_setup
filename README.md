# jetson_setup

The following commands were tested on Jetson Xavier Nx.

## CUDA, CUDNN, TensorRT
```sh
sudo apt install nvidia-jetpack
```
add environmental variables
```sh
gedit ~/.bashrc

# add to the end of file, and please care about your version !
export CUDA_HOME=/usr/local/cuda
export LD_LIBRARY_PATH=/usr/local/cuda/lib64:$LD_LIBRARY_PATH
export PATH=/usr/local/cuda/bin:$PATH

source ~/.bashrc
```

## jetson tool
```sh
sudo apt install python3-pip
sudo -H pip3 install -U jetson-stats

# launch
sudo jtop
```

## coding tool
```sh
sudo apt install cmake git curl net-tools terminator
```

## ROS
```sh
# Setup your computer to accept software from packages.ros.org.
sudo sh -c '. /etc/lsb-release && echo "deb http://mirrors.ustc.edu.cn/ros/ubuntu/ `lsb_release -cs` main" > /etc/apt/sources.list.d/ros-latest.list'
# Set up your keys
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -

sudo apt update
sudo apt install ros-noetic-desktop-full
echo "source /opt/ros/noetic/setup.zsh" >> ~/.zshrc
source ~/.zshrc
```
