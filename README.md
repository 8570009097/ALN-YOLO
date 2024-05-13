# Official ALN-YOLO

Shocking! This is an Image-Adaptive Lightweight Detector for Small Target Detection in Complex Environments.

Implementation of paper - [Run efficiently:An Image-Adaptive Lightweight Detector for Small Target Detection in Complex Environments]


<div align="center">
    <a href="./">
        <img src="https://github.com/8570009097/ALN-YOLO/blob/main/ALN-YOLOs.png" width="79%"/>
    </a>
</div>



## Performance 

MS COCO

| Model | Test Size | AP<sup>test</sup> | AP<sub>50</sub><sup>test</sup> |Params | FLPOs | batch 32 average time |
| :-- | :-: | :-: | :-: | :-: | :-: | :-: |
| [**YOLOv5-N**] | 640 | **28.0%** | **45.7%** | 1.9 *M* | 4.5 *G* |735 *fps*|
| [**YOLOv7-Tiny**] | 640 | **33.3%** | **49.9%** |6.2 *M* |5.8 *G* |1175 *fps*|
|  |  |  |  |  |  |  |
| [**YOLOv8-N**]| 640 | **37.3%** | **52.6%** | 3.2 *M* | 8.7 *G* |734 *fps*|
| [**Gold-YOLO-N**] | 640 | **39.9%** | **55.9%** | 5.6 *M* | 12.1*G* |1030 *fps*|
| [**YOLOv9-N**] | 640 | **38.1%** | **52.9%** | 2.2 *M* | 8.3 *G* |450 *fps*|
| [**ALN-YOLOs**] | 640 | **37.8%** | **56.2%** | 5.7 *M* | 12.5 *G* |1176 *fps*|



## Installation

install requirements
<details><summary> <b>Expand</b> </summary>

``` shell

# pip install required packages
pip install -r requirements.txt

# go to code folder
cd /ALN-YOLO
```
</details>

## Eval
change the data/coco.yaml to your data path

eval ALN-YOLO

``` shell
python test.py --data data/coco.yaml --img 640 --batch 32 --conf 0.001 --iou 0.65 --device 0 --weights ALN-YOLOs.pt
```

You will get the results:

```
 claa = all
 Image = 4952
 labels = 0.646
 P = 0.646
 R = 0.526
 mAP@.5 = 0.562
 mAP@.5:.95: 100% = 0.345
 Speed = 0.9ms
 Model = 5693858
 GFLOPs=12.5
```
