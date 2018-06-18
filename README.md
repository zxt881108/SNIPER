# SNIPER: Efficient Multi-Scale Training

<p align="center">
<img src="https://github.com/mahyarnajibi/SNIPER/blob/master/data/demo/readme_figs/sniper.gif" />
 </p>

SNIPER is an efficient multi-scale training approach for instance-level recognition tasks like object detection and instance-level segmentataion. 
Instead of processing all pixels in an image pyramid, SNIPER selectively processes context regions around the ground-truth objects (a.k.a *chips*).
This significantly speeds up multi-scale training as it operates on low-resolution chips. 
Due to its memeory efficient design, SNIPER can benefit from *Batch Normalization* during training and it makes larger batch-sizes possible for instance-level recognition tasks on a single GPU. Hence, we do not need to synchronize batch-normalization statistics across GPUs and we can train object detectors similar to the way we do image classification!

[SNIPER](https://arxiv.org/abs/1805.09300) is described in the following paper:
<pre>
<b>SNIPER: Efficient Multi-Scale Training</b>
<b>Bharat Singh*, Mahyar Najibi*, and Larry S. Davis (* denotes equal contribution)</b>
<b>arXiv preprint arXiv:1805.09300, 2018.</b>
</pre>


### License
SNIPER is released under Apache license. See LICENSE for details.


### Installation
Please refer to the master branch for installation instructions.
<a name="demo"> </a>

### Training
SNIPER makes it possible to directly train on the OpenImages dataset from scratch. For training the model with default configs you can use the following script:
```
python main_chips_open.py
```

Please note that while the branch is able to reproduce the results, it is out of sync with the master branch and would be updated soon.
