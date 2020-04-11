# How to find which version of TensorFlow is installed in my system? ?

```bash
python -c 'import tensorflow as tf; print(tf.__version__)'  # for Python 2
python3 -c 'import tensorflow as tf; print(tf.__version__)'  # for Python 3
```

# TensorFlow Object Detection API tutorial
### Install Tensor Flow 2.x
```bash
pip3 install -U --pre tensorflow=="2.*"
```
### Make sure you have pycocotools installed
```bash
pip install pycocotools
```

Then Download models Folder from 
https://github.com/tensorflow/models

and extract your zip file under TensorFlow folder 
```
   TensorFlow
    └─ models
        ├── official
        ├── research
        ├── samples
        └── tutorials

```

# Protobuf Installation/Compilation
 
Download the latest protoc-*-*.zip release :
https://github.com/protocolbuffers/protobuf/releases

Then Extract the contents of the downloaded protoc-*-*.zip in a directory in your system .

Enter into TensorFlow/models/research/ folder 

```bash
cd TensorFlow/models/research/
```
and then run this command :
```bash
protoc object_detection/protos/*.proto --python_out=.
```

Install the Tensorflow\models\research\object_detection package by running the following from Tensorflow\models\research:
```bash
cd TensorFlow/models/research/
pip install .
```

#pycocotools Installation :
```bash
pip3 install git+https://github.com/philferriere/cocoapi.git#subdirectory=PythonAPI
```

#Test Installation :

```python
import cv2
import numpy as np
import tensorflow as tf
from object_detection.utils import label_map_util
from object_detection.utils import ops as utils_ops
from object_detection.utils import visualization_utils as vis_util
```



#### references :

object detection tutorial : https://github.com/tensorflow/models/blob/master/research/object_detection/object_detection_tutorial.ipynb

TensorFlow : https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/install.html

Article : https://www.actuia.com/contribution/jeancharlesrisch/segmentation-et-detection-dobjets-en-temps-reel-avec-tensorflow/

Code main Github :https://github.com/jcRisch/Real_Time_Pixel_Segmentation





