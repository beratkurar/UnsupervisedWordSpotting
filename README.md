### Installations for running keras-tensoflow on GPU
1. Upgrade pip and install opencv2
```
cd ~
pip install --upgrade pip
pip install opencv-python
```
2. Upgrade keras and set tensorflow background
```
pip uninstall keras
pip install keras==2.1.2
pip uninstall python-dateutil
pip install python-dateutil
vi ~/.keras/keras.json
  {
    "backend": "tensorflow",
    "image_data_format": "channels_last",
    "floatx": "float32",
    "epsilon": 1e-07
  }
```
3. Uninstall tensorflow and install tensorflow-gpu which is necessary to run on GPU
```
pip uninstall tensorflow
pip install tensorflow-gpu==1.2
```
5. Run python on a specific GPU
```
import os
os.environ["CUDA_VISIBLE_DEVICES"]="2"
```

### How to run the project
1. Train and test
```
python3 siam13.py
```
