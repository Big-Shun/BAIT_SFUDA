# BAIT_SFUDA

Code (pytorch) for ['Unsupervised Domain Adaptation without Source Data by Casting a BAIT'](https://arxiv.org/abs/2010.12427) on VisDA. **If for Office-Home and Office-31, please use learning rate 10 times larger.**

**TL;DR: We extend MCD to source-free domain adaptation.**

### Preliminary
You need to download the [VisDA](https://github.com/VisionLearningGroup/taskcv-2017-public/tree/master/classification) dataset.

Our codes are using PyTorch 1.3.1, torchvision 0.4.2 (python 3.7.6). The experiments are conducted on one GPU (RTX6000).


### Training and evaluation

1. First training model on the source data.

> python train_source.py

2. Then adapting source model to target domain, with only the unlabeled target data.

> python train_target.py


### Results in paper
![VisDA](/img/visda.png)

**The result of SHOT is from the ICML [camera-ready version](https://proceedings.icml.cc/static/paper_files/icml/2020/194-Paper.pdf).**

### Acknowledgement

The codes are based on [SHOT (ICML 2020, also source-free)](https://github.com/tim-learn/SHOT).

