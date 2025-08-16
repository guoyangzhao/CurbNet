# CurbNet
## CurbNet: Curb Detection Framework Based on LiDAR Point Cloud Segmentation
[![arxiv paper](https://img.shields.io/badge/arXiv-Paper-red)](https://arxiv.org/abs/2403.16794)
<br>

### Method:
**Curb detection challenges and our proposed method.** Three main challenges of curb detection are shown (a) height feature extraction (b) different density distribution of point clouds (c) Curb point cloud quantity proportion imbalance. Solution: First propose a 3D-Curb dataset. The MSCA module is designed for multi-scale spatial feature fusion and height feature extraction. The loss group is proposed to solve the imbalance problem. Finally, we use post-processing to further improve performance.

<img src="https://github.com/guoyangzhao/CurbNet/blob/main/images/cover-figure527.png" width="40%" height="auto">

### Framework:

<img src="https://github.com/guoyangzhao/CurbNet/blob/main/images/framework527.png" width="60%" height="auto">

### Detection Results in SemanticKITTI Dataset:

<img src="https://github.com/guoyangzhao/CurbNet/blob/main/images/3Dcurb-no-occ2.png" width="50%" height="auto">


## 3D-Curb Datasets:
We have developed and proposed the **3D-Curb dataset** based on the large-scale, open-source **SemanticKITTI dataset**, adding a new curb category with 3D label, while retaining the other original 28 semantic categories. This dataset was collected using a 64-line LiDAR, providing a comprehensive view of various street scenes as a universal autonomous driving dataset.

<img src="https://github.com/guoyangzhao/CurbNet/blob/main/images/Dataset_construct527.png" width="50%" height="auto">

- Our dataset can be visualized using SemanticKITTI **[API](https://github.com/PRBonn/semantic-kitti-api)**

- You can download the 3D-Curb dataset through Baidu Netdisk **[HERE](https://pan.baidu.com/s/1YKtiCdgugzTxHD6dTpXNHQ)**, and the extraction code is 1234. Or from Google Drive **[HERE](https://drive.google.com/file/d/18rK1TE96SfWMi2GjK0RO1U4UPxumA1-E/view?usp=sharing)**

- The annotation of the 3D-Curb dataset is based on the SemanticKITTI format. The point cloud file is stored in the **.bin** file and the label is in the corresponding **.label** file.


### Attention: 

Because the Curb category is additionally added, we set the Curb labels category to 3. Therefore, when using API visualization, please add **3: "curb"** to **label:** in **config/semantic-kitti.yaml** to increase the visualization of curb.


### Data organization:

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

### NRS Dataset: 

The original NRS dataset mentioned in the paper only has 2D labels. We project the 2D labels onto a 3D point cloud for processing and convert the data format to the same as SemanticKITTI. We have also made the processed NRS dataset public and can also be downloaded from Baidu Netdisk **[HERE](https://pan.baidu.com/s/1U6b5c6TxfruNT572_vwLYA)**, and the extraction code is 1234. Or from Google Drive **[HERE](https://drive.google.com/file/d/1kAj1xEHnppwrg2zLp42rCsLL8439glhy/view?usp=sharing)**

## Citations:
If you find CurbNet or 3D-Curb Dataset useful in your research or applications, please consider giving us a star 🌟 and citing it.

```bibtex
@article{zhao2024curbnet,
  title={CurbNet: Curb Detection Framework Based on LiDAR Point Cloud Segmentation},
  author={Zhao, Guoyang and Ma, Fulong and Liu, Yuxuan and Qi, Weiqing and Liu, Ming and Ma, Jun},
  journal={arXiv preprint arXiv:2403.16794},
  year={2024}
}
```

