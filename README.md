Addressing Domain Discrepancy: A Dual-branch Collaborative Model to Unsupervised Dehazing
===========================

Abstract
===========================

Although synthetic data can alleviate acquisition challenges in image dehazing tasks, it also introduces the problem of domain bias when dealing with small-scale data. This paper proposes a novel dual-branch collaborative unpaired dehazing model (DCM-dehaze) to address this issue. The proposed method consists of two collaborative branches: dehazing and contour constraints. Specifically, we design a dual depthwise separable convolutional module (DDSCM) to enhance the information expressiveness of deeper features and the correlation to shallow features. In addition, we construct a bidirectional contour function to optimize the edge features of the image to enhance the clarity and fidelity of the image details. Furthermore, we present feature enhancers via a residual dense architecture to eliminate redundant features of the dehazing process and further alleviate the domain deviation problem. Extensive experiments on benchmark datasets show that our method reaches the state-of-the-art.

Prerequisites
===========================
Python 3.7 + Pytorch, please refer environment.yml for detiled requirments.

Preparation
===========================
## Install
Python 3.7 + Pytorch, please refer 'environment.yml' for detiled requirments.
You can create a new conda environment:
```
conda env create -f environment.yml
```

Datasets
===========================
We used [SOTS-indoor](https://sites.google.com/view/reside-dehaze-datasets/reside-v0), [SOTS-outdoor](https://sites.google.com/view/reside-dehaze-datasets/reside-v0)  and [I-HAZE](https://data.vision.ee.ethz.ch/cvl/ntire18//i-haze/) for testing.  

For training, we used [ITS](https://sites.google.com/view/reside-dehaze-datasets/reside-standard) dataset, you can follow the operations above to generate the training file lists.

Train
===========================
You can modify the training settings for each experiment in the 'configs.yml'. Then run the following script to train the model：
```
python train.py --model （Model class） --checkpoints （Training sample address）
```

For example, we train the DCM-dehaze on the [ITS](https://sites.google.com/view/reside-dehaze-datasets/reside-standard)：
```
python train.py --model 1 --checkpoints ./checkpoints/train_example
```
Such as SOTS-indoor, you can download the pretrained models on [Training weight](https://pan.baidu.com/s/1dghKt-Dasr5XM_0VOF4miQ)(bzyx).

Test
===========================
Run the following script to test the trained model：
```
python test.py --model （Model class） --checkpoints （Test sample address）
```
For example, we test the DCM-dehaze on the SOTS-indoor set:
```
python test.py --model 1 --checkpoints ./checkpoints/test_example
```

Warm Reminder
===========================
Some important hyperparameters and training parameters in the code are shown in ‘config.yml’ .
