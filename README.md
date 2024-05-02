# CurbNet
## CurbNet: Curb Detection Framework Based on LiDAR Point Cloud Segmentation
[![arxiv paper](https://img.shields.io/badge/arXiv-Paper-red)](https://arxiv.org/abs/2403.16794)
<br>

### Method:
**Curb detection challenges and our proposed method.** Three main challenges of curb detection are shown (a) height feature extraction (b) different density distribution of point clouds (c) Curb point cloud quantity proportion imbalance. Solution: First propose a 3D-Curb dataset. The MSCA module is designed to extract features of the xy, xz and yz planes and perform multi-feature fusion. The loss group is proposed to solve the imbalance problem. Finally, we use post-processing to further improve performance.
![CurbNet-Method](https://github.com/guoyangzhao/CurbNet/blob/main/images/cover-figure2.png)

### Framework:
![CurbNet-Framework](https://github.com/guoyangzhao/CurbNet/blob/main/images/framework.png)

### Detection Results in SemanticKITTI Dataset:
![CurbNet-Result](https://github.com/guoyangzhao/CurbNet/blob/main/images/3Dcurb-no-occ2.png)


## 3D-Curb Datasets:
We have developed and proposed the **3D-Curb dataset** based on the large-scale, open-source **SemanticKITTI dataset**, adding a new curb category with 3D label, while retaining the other original 28 semantic categories. This dataset was collected using a 64-line LiDAR, providing a comprehensive view of various street scenes as a universal autonomous driving dataset.

Our dataset can be visualized using **SemanticKITTI [API](https://github.com/PRBonn/semantic-kitti-api)**

The download link for the 3D-Curb dataset is **[HERE]()**.
