# storage

#### Poseidon for Ubuntu

Prior to installation, make sure you have installed CUDA and cuDNN from the [Nvidia website](https://developer.nvidia.com/cuda-downloads).

CUDA installation instructions are straightforward on the website.

Get [cuDNN](https://developer.nvidia.com/cudnn) (you will need to create an Nvidia account if you don't have one).

Choose the cuDNN distribution that matches your CUDA installation. Version 5.1 works great for me (provided your CUDA version is > 7.0).
Finally, download cuDNN <version> Library for Linux.

Installing cuDNN after download:
Say your cuDNN file is called `cudnn-8.0-linux-x64-v5.1.tar`.
```bash
sudo cp cudnn-8.0-linux-x64-v5.1.tar /usr/local
sudo tar -xf /usr/local/cudnn-8.0-linux-x64-v5.1.tar
```

To install poseidon (for Ubuntu14 and Ubuntu16) run the following commands:
```bash
wget https://github.com/sailing-pmls/storage/raw/master/poseidon/deb/ubuntu/poseidon-repo-ubuntu_0.10_amd64.deb
sudo dpkg -i poseidon-repo-ubuntu_0.10_amd64.deb
sudo apt-get update
sudo apt-get install poseidon
```

Before running tensorflow, make sure to set your CUDA environment variables (you can also append this to your .bashrc file):
```bash
export CUDA_HOME=/usr/local/cuda && export LD_LIBRARY_PATH=${LD_LIBRARY_PATH}:/usr/local/cuda/lib64
python
>>> import tensorflow as tf
. . .
```
