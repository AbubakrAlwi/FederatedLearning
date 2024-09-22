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
  3. update Conda
  ```shell
   conda update -n base -c defaults conda
  ```
  5. Create then activate the new environment :
  ```shell 
   conda create -n env_name  python=3.9
   conda activate env_name
 ```
 6. Install Required Libraries:
  ```shell
   pip install -r requirements.txt
 ```
Then, to verify that everything works correctly you can run the following command:

```shell
python -c "import flwr;print(flwr.__version__)"
```

If you don't see any errors you're good to go!

Note : For the server side we apply the same steps .

______________________________________________________________________
## Run Federated Learning with PyTorch and Flower

Afterwards you are ready to start the Flower server as well as the clients. You can simply start the server in a terminal as follows:

```shell
python3 server.py
```
Now you are ready to start the Flower clients which will participate in the learning. We need to specify the partition id to
use different partitions of the data on different nodes.  To do so simply open two more terminal windows and run the
following commands.
Now you are ready to start the Flower clients which will participate in the learning. We need to specify the partition id to
use different partitions of the data on different nodes.  To do so simply open two more terminal windows and run the
following commands.

Start client 1 in the first terminal:

```shell
python3 client.py --partition-id 0
```

Start client 2 in the second terminal:

```shell
python3 client.py --partition-id 1
```


