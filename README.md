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
