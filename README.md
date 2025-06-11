# SPN : Official Project Webpage
This repository provides the official PyTorch implementation of the following paper:
> [**Stochastic Prompt Network for Sim-To-Real Generalization**]<br>
> Yao Li, Jinlong Shi, Yun Cui, Dan Xua, Wei Tenga, Yan Jiang  <br>
>School of Computer Science, Jiangsu University of Science and Technology, Zhenjiang 212000, China<br>
>School of Material Design and Engineering, Beijing institute of Fashion Technology,Beijing, 100029, China

> **Abstract:**
> *Due to the significant domain differences between synthetic data and real data, this is a challenging problem for current domain generalized segmentation networks. Therefore, we propose a stochastic prompt network (SPN) for sim-to-real transfer, which first uses multiple resolution inputs in the encoder to effectively combine coarse-grained and fine-grained information. Then, the hybrid prompts are added by the multi-scale fusion feature stochastic prompt network (MSFFP) to enhance the model's immunity to semantic noise and extract more domain-invariant features. Experimental results show that our SPN can effectively enhance the model's generalization ability to unseen data. In terms of mean intersection over union (mIoU) metric, compared with SOTA, the SPN improves by 3.86\% and 2.05\% respectively on two real scene-enhanced datasets (Rain\_Cityscapes, Foggy\_Cityscapes), and an average improvement of 1.48\% on four conventional datasets (BDD100k, Cityscapes, Mapillary, Synthia). Our project can be found at https://github.com/leo-lab-511/SPN.* <br>

<p align="center">
  <img src="Figure2.jpg" />
</p>

We advise you to use conda environment to run the package. Run the following command to install all the necessary modules:

```sh
conda env create -f SPN.yml 
conda activate SPN
```


### How to Run SPN
We trained the model on [GTAV](https://download.visinf.tu-darmstadt.de/data/from_games/)
We evaluated the model on [Cityscapes](https://www.cityscapes-dataset.com/), [BDD-100K](https://bair.berkeley.edu/blog/2018/05/30/bdd/), [Synthia](https://synthia-dataset.net/downloads/) ([Foggy Cityscapes](http://synthia-dataset.net/download/808/)), [Rain Cityscapes](https://www.cityscapes-dataset.com/) and [Mapillary](https://www.mapillary.com/dataset/).

We adopt Class uniform sampling proposed in [this paper](https://openaccess.thecvf.com/content_CVPR_2019/papers/Zhu_Improving_Semantic_Segmentation_via_Video_Propagation_and_Label_Relaxation_CVPR_2019_paper.pdf) to handle class imbalance problems.


1. For Cityscapes dataset, download "leftImg8bit_trainvaltest.zip" and "gtFine_trainvaltest.zip" from https://www.cityscapes-dataset.com/downloads/<br>
Unzip the files and make the directory structures as follows.
```
Cityscapes
 └ leftImg8bit_trainvaltest
   └ leftImg8bit
     └ train
     └ val
     └ test
 └ gtFine_trainvaltest
   └ gtFine
     └ train
     └ val
     └ test
```
2. For BDD-100k dataset, download  from https://www.mapillary.com/dataset/<br>
Unzip the files and make the directory structures as follows.
```
BDD-100k
 └ images
   └ train
   └ val
   └ test
 └ labels
   └ train
   └ val
```
3. For Mapillary dataset, download  from https://bair.berkeley.edu/blog/2018/05/30/bdd/<br>
```
Mapillary
 └ training
   └ images
   └ labels
 └ validation
   └ images
   └ labels
 └ test
   └ images
   └ labels
```
### Routine Scenario Generalization Visualization
<p align="center">
  <img src="Figure5.jpg" />
</p>


1. For Rain_Cityscapes dataset, download from https://www.cityscapes-dataset.com/downloads/<br>
Unzip the files and make the directory structures as follows.
```
Rain_Cityscapes
 └ leftImg8bit_trainvaltest
   └ leftImg8bit
     └ train
     └ val
     └ test
 └ gtFine_trainvaltest
   └ gtFine
     └ train
     └ val
     └ test
```
1. For Foggy_Cityscapes dataset, download  from https://www.cityscapes-dataset.com/downloads/<br>
Unzip the files and make the directory structures as follows.
```
Foggy_Cityscapes
 └ leftImg8bit_trainvaltest
   └ leftImg8bit
     └ train
     └ val
     └ test
 └ gtFine_trainvaltest
   └ gtFine
     └ train
     └ val
     └ test
```


### Enhanced Scenario Generalization Visualization
<p align="center">
  <img src="Figure6.jpg" />
</p>
 
### Segmentation AAbility Comparison of State of Art Model
<p align="center">
  <img src="Figure7.jpg" />
</p>
## Terms of Use
This software is for non-commercial use only.
The source code is released under the Attribution-NonCommercial-ShareAlike (CC BY-NC-SA) Licence
(see [this](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode) for details)