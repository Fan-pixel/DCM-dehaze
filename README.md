Addressing Domain Discrepancy: A Dual-branch Collaborative Model to Unsupervised Dehazing
===========================

Abstract
===========================

Although synthetic data can alleviate acquisition challenges in image dehazing tasks, it also introduces the problem of domain bias when dealing with small-scale data. This paper proposes a novel dual-branch collaborative unpaired dehazing model (DCM-dehaze) to address this issue. The proposed method consists of two collaborative branches: dehazing and contour constraints. Specifically, we design a dual depthwise separable convolutional module (DDSCM) to enhance the information expressiveness of deeper features and the correlation to shallow features. In addition, we construct a bidirectional contour function to optimize the edge features of the image to enhance the clarity and fidelity of the image details. Furthermore, we present feature enhancers via a residual dense architecture to eliminate redundant features of the dehazing process and further alleviate the domain deviation problem. Extensive experiments on benchmark datasets show that our method reaches the state-of-the-art.

![图片1](https://github.com/Fan-pixel/DCM-dehaze/blob/main/fig_3.pdf)

Datasets
===========================
We used [SOTS-indoor](https://sites.google.com/view/reside-dehaze-datasets/reside-v0), [SOTS-outdoor](https://sites.google.com/view/reside-dehaze-datasets/reside-v0)  and [I-HAZE](https://data.vision.ee.ethz.ch/cvl/ntire18//i-haze/) for testing.  

For training, we used [ITS](https://sites.google.com/view/reside-dehaze-datasets/reside-standard) dataset, you can follow the operations above to generate the training file lists.
