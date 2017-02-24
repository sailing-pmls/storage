# storage

#### Poseidon for Ubuntu

Prior to installation, make sure you have installed CUDA and cuDNN from the [Nvidia website](https://developer.nvidia.com/cuda-downloads).

CUDA installation instructions are straightforward on the website.

Get [cuDNN](https://developer.nvidia.com/cudnn) (you will need to create an Nvidia account if you don't have one).

Choose the cuDNN distribution that matches your CUDA installation. Version 5.1 works great for me (provided your CUDA version is > 7.0).
Finally, download cuDNN <version> Library for Linux.

Installing cuDNN after download:
Say your cuDNN file is called `cudnn-8.0-linux-x64-v5.1.tgz`.
```bash
sudo gunzip cudnn-8.0-linux-x64-v5.1.tgz
sudo cp cudnn-8.0-linux-x64-v5.1.tar /usr/local
sudo tar -xf /usr/local/cudnn-8.0-linux-x64-v5.1.tar
sudo rm /usr/local/cudnn-8.0-linux-x64-v5.1.tar
```

To install poseidon run the following commands:
```bash
wget https://github.com/sailing-pmls/storage/raw/master/poseidon/deb/ubuntu14/poseidon-repo-u14.deb
sudo dpkg -i poseidon-repo-u14.deb
sudo apt-get update
sudo apt-get install poseidon
```
