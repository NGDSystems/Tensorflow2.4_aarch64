# Tensorflow2.4
Follow the follwoing steps to install Python3.7:
```
sudo apt update
yes "" | sudo apt install software-properties-common
yes "" | sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt install python3.7 -y
```
Set Python3.7 as default python3:
```
sudo update-alternatives --install /usr/bin/python3 python /usr/bin/python3.7 1
sudo update-alternatives --config python
```
Install pip for python3:
```
wget https://bootstrap.pypa.io/get-pip.py
python3 get-pip.py 
export PATH="~/.local/bin:$PATH"
```
Download and install the following prebuilt .whl files:
```
wget https://github.com/lhelontra/tensorflow-on-arm/releases/download/v2.4.0/tensorflow-2.4.0-cp37-none-linux_aarch64.whl
wget https://github.com/NGDSystems/Tensorflow2.4/raw/main/files/grpcio-1.32.0-cp37-cp37m-linux_aarch64.whl
wget https://github.com/NGDSystems/Tensorflow2.4/raw/main/files/h5py-2.10.0-cp37-cp37m-linux_aarch64.whl
pip3 install grpcio-1.32.0-cp37-cp37m-linux_aarch64.whl
pip3 install h5py-2.10.0-cp37-cp37m-linux_aarch64.whl
pip3 install tensorflow-2.4.0-cp37-none-linux_aarch64.whl
```
Check if the installation was succcessfull:
```
python3 -c 'import tensorflow as tf; print(tf.__version__)'
```
download and run a sample application.
```
python3 example.py
```

Output:
```
Epoch 1/5
1875/1875 [==============================] - 20s 10ms/step - loss: 0.4736 - accuracy: 0.8616
Epoch 2/5
1875/1875 [==============================] - 18s 10ms/step - loss: 0.1508 - accuracy: 0.9553
Epoch 3/5
1875/1875 [==============================] - 18s 10ms/step - loss: 0.1122 - accuracy: 0.9674
Epoch 4/5
1875/1875 [==============================] - 18s 10ms/step - loss: 0.0884 - accuracy: 0.9734
Epoch 5/5
1875/1875 [==============================] - 18s 10ms/step - loss: 0.0727 - accuracy: 0.9775
313/313 - 2s - loss: 0.0749 - accuracy: 0.9775
```
