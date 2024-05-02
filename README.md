# CurbNet
## CurbNet: Curb Detection Framework Based on LiDAR Point Cloud Segmentation
[![arxiv paper](https://img.shields.io/badge/arXiv-Paper-red)](https://arxiv.org/abs/2403.16794)
<br>

### Method:
**Curb detection challenges and our proposed method.** Three main challenges of curb detection are shown (a) height feature extraction (b) different density distribution of point clouds (c) Curb point cloud quantity proportion imbalance. Solution: First propose a 3D-Curb dataset. The MSCA module is designed to extract features of the xy, xz and yz planes and perform multi-feature fusion. The loss group is proposed to solve the imbalance problem. Finally, we use post-processing to further improve performance.

<img src="https://github.com/guoyangzhao/CurbNet/blob/main/images/cover-figure2.png" width="40%" height="auto">

### Framework:

<img src="https://github.com/guoyangzhao/CurbNet/blob/main/images/framework.png" width="60%" height="auto">

### Detection Results in SemanticKITTI Dataset:

<img src="https://github.com/guoyangzhao/CurbNet/blob/main/images/3Dcurb-no-occ2.png" width="50%" height="auto">


## 3D-Curb Datasets:
We have developed and proposed the **3D-Curb dataset** based on the large-scale, open-source **SemanticKITTI dataset**, adding a new curb category with 3D label, while retaining the other original 28 semantic categories. This dataset was collected using a 64-line LiDAR, providing a comprehensive view of various street scenes as a universal autonomous driving dataset.

- Our dataset can be visualized using SemanticKITTI **[API](https://github.com/PRBonn/semantic-kitti-api)**

- The download link for the 3D-Curb dataset is **[HERE](https://drive.google.com/drive/folders/1u2PrRg6AsZCnDkZQS-GDA3N10olEmiD2?usp=sharing)**.

- The annotation of the 3D-Curb dataset is based on the SemanticKITTI format. The point cloud file is stored in the **.bin** file and the label is in the corresponding **.label** file.


### Attention: 

Because the Curb category is additionally added, we set the Curb labels category to 3. Therefore, when using API visualization, please add **3: "curb"** to **label:** in **config/semantic-kitti.yaml** to increase the visualization of curb.


### Data organization

The data is organized in the following format:

```
/kitti/dataset/
          └── sequences/
                  ├── 00/
                  │   ├── labels/
                  │   │     ├ 000000.label
                  │   │     └ 000001.label
                  │   └── velodyne/
                  │         ├ 000000.bin
                  │         └ 000001.bin
                  ├── 01/
                  ├── 02/
                  .
                  └── 10/
```
