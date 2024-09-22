# Federated learning On RasberryPi     
This project implements a Federated learning using the federated learning library Flower . It is demonstrated through RasberryPi 5 and RasberryPi 4 as clients.
# Getting Started
## Setting Up Raspberry Pi Devices
 Update System Packages
  ```shell
    sudo apt-get update && sudo apt-get upgrade -y
 ```
 Set Up a Conda Virtual Environment
   1. install conda For Raspberry Pi OS 64-bit :
  ```shell
    mkdir -p ~/miniconda3
    wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-aarch64.sh -O ~/miniconda3/miniconda.sh
    bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
    rm ~/miniconda3/miniconda.sh  
 ```
  2. Activate Conda:
 ```shell
    ~/miniconda3/bin/conda init bash 
 ```
  OR if you using zsh bash :
  
  ```shell
   ~/miniconda3/bin/conda init zsh 
 ```

  3. create virtual environment:
  ```shell
   conda update -n base -c defaults conda  
   conda create -n env_name  python=3.9
   conda activate env_name
 ```
 4. Install Required Libraries:
  ```shell
   pip install -r requirements.txt
 ```




