# YOLOv5_voc
In this repository we want to train YOLOv5 on VOC dataset.

<details open>
<summary>Install</summary>
Clone the repo and install requirement packages

```
git clone https://github.com/ultralytics/yolov5  # clone
cd yolov5
pip install -r requirements.txt  # install
```
</details>

<details open>
<summary>Inference</summary>

```
import torch

# Model
model = torch.hub.load('ultralytics/yolov5', 'yolov5s')  # or yolov5m, yolov5l, yolov5x, custom

# Images
img = 'https://ultralytics.com/images/zidane.jpg'  # or file, Path, PIL, OpenCV, numpy, list

# Inference
results = model(img)

# Results
results.print()  # or .show(), .save(), .crop(), .pandas(), etc.
```

</details>


<details open>
<summary>Training</summary>

The below command reproduces YOLOv5 VOC results. Models and datasets download automatically from the latest YOLOv5 release

```
python train.py --data VOC.yaml --cfg yolov5n.yaml --weights '' --batch-size 128
                                       yolov5s                                64
                                       yolov5m                                40
                                       yolov5l                                24
                                       yolov5x                                16
```

</details>
