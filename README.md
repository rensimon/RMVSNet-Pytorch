# R-MVSNet Pytorch

## Installation

```
pip install git+git://github.com/leejaeyong7/rmvsnet-pytorch.git#egg=rmvsnet
```

## Usage

```python
import rmvsnet

'''

Args: 
  images: Nx3xHxW tensor
  intrinsics: Nx3x3 tensor
  extrinsics: Nx4x4 tensor
  depth_start: float
  depth_interval: float
  depth_num: float

  depth ranges are computed by: depth_start + range(depth_num) * depth_interval

Return:
  probs: tensor of shape 1xDx(H/4)x(W/4)
'''

probs = rmvsnet(images, intrinsics, extrinsics, depth_start, depth_interval, depth_num)
```

## Reference:

## About
This is a custom port of [Original MVSNet using Tensorflow](https://github.com/YoYo000/MVSNet) in Pytorch.
We use same weight that the authors provided (GRU).
```
@article{yao2019recurrent,
  title={Recurrent MVSNet for High-resolution Multi-view Stereo Depth Inference},
  author={Yao, Yao and Luo, Zixin and Li, Shiwei and Shen, Tianwei and Fang, Tian and Quan, Long},
  journal={Computer Vision and Pattern Recognition (CVPR)},
  year={2019}
}
```

