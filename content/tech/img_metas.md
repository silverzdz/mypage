---
title: "img_metas"
date: 2023-03-07T14:37:09+08:00
# weight: 1
# aliases: ["/first"]
tags: ["hdmap"]
author: "silverxb"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "nuScenes data's img_metas for MapTR inference"
canonicalURL: "http://silverxb.xyz/img_metas"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
ShowCodeCopyButtons: true
cover:
    # image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/silverzdz/mypage/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

```python
img_metas = data['img_metas'][0].data[0][0]
```

| 数据项 | type | size[len] | default | 备注 | 必需 |
| ------ | ---- | --------- | ------- | ---- | ---- | 
| filename | list(str) | [6] | | 六个视角图片文件名 | False |
| ori_shape | list(tuple) | 3[6] | (450, 800, 3) | 原始尺寸 | False |
| img_shape | list(tuple) | 3[6] | (480, 800, 3) | 图片尺寸 | False |
| lidar2img | list(array) | (4,4)[1] | | 雷达到相机坐标矩阵 | False | 
| pad_shape | list(tuple) | 3[6] | (480, 800, 3) | 填充尺寸 | False |
| scale_factor | float | | 1.0 | 比例因子 | False |
| flip | bool | | False | 翻转 | False |
| pcd_horizontal_flip | bool | | False | 点云水平翻转 | False |
| pcd_vertical_flip | bool | | False | 点云垂直翻转 | False |
| box_mode_3d | <Box3DMode.LIDAR> | | 0 | 类内static | False |
| box_type_3d | <class 'mmdet3d.core.bbox.structures.lidar_box3d.LiDARInstance3DBoxes'> | | | 雷达坐标系物体的3D Box | False |
| img_norm_cfg | dict{'mean': array(dtype=float32), 'std': array(dtype=float32) } | (3,), (3,) | | 图片均值方差 | False |
| sample_idx | str | | | sample的index | False |
| prev_idx | str | | | 前一个sample的index | False |
| next_idx | str | | | 后一个sample的index | False |
| pcd_scale_factor | float | | 1.0 | 点云比例因子 | False |
| pts_filename | str | | | 点云文件名 | False |
| scene_token | str | | | 场景token | False |
| can_bus | array | (18,) | | 车辆can_bus底层数据 | True |
| lidar2global | array | (4,4) | | 雷达到世界坐标矩阵 | False | 
| camera_intrinsics | list(array) | (4,4)[6] | | 相机内参矩阵 | False |
| img_aug_matrix | list(array) | (4,4)[6] | diag[0.5, 0.5, 1, 1] | 图像增强矩阵 | False |
| lidar2ego | array | (4,4) | | 雷达到车辆姿态ego坐标矩阵 | False |