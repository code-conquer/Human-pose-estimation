##  Human Pose Estimation with HRNet

This repository provides:
- Huamn pose estimation ``HRNet`` implementation in PyTorch (>=1.0).
- A simple class (``HRNet``) that loads the HRNet network for the human pose estimation, loads the pre-trained weights,
 and make human predictions on a single image or a batch of images.
- Multi-person support with ``Yolo-v3``(enabled by default).  
- A reference code that runs a live demo reading frames from a webcam or a video file.
 

#### Running the live demo

From a connected camera:
```
python scripts/live-demo.py --camera_id 0
```
From a saved video:
```
python scripts/live-demo.py --filename video.mp4
```

For help:
```
python scripts/live-demo.py --help
```

#### Running the training script

```
python scripts/train_coco.py
```

For help:
```
python scripts/train_coco.py --help
```

#### Requirements

- Install the required packages    
 ``pip install -r requirements.txt``
- Download HRNet pre-trained weights from 
[https://stduestceducn-my.sharepoint.com](https://stduestceducn-my.sharepoint.com/:u:/g/personal/201921080433_std_uestc_edu_cn/EU7F-XTMJSRKgZw2WnvT1cUBDGUMG_F-4jev_8A41k4F5g?e=eeHcY6)
- Download Yolo's pre-trained weights running the script ``download_weights.sh`` from the ``models/detectors/yolo/weights`` folder
- (Optional) Download the [COCO dataset](http://cocodataset.org/#download) and save it in ``./datasets/COCO``
    - Your folders should look like:
        ```
        human_pose_estimation
        ├── datasets                (datasets - for training only)
        ├── losses                  (loss functions)
        ├── misc                    (misc)
        ├── models                  (pytorch models)
        │  └── detectors            (people detectors)
        │    └── yolo               (PyTorch-YOLOv3 repository)
        │      ├── ...
        │      └── weights          (YOLOv3 weights)
        ├── scripts                 (scripts)
        ├── testing                 (testing code)
        ├── training                (training code)
        └── weights                 (HRnet weights)
        ```
    
