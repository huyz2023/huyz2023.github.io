---
title: "Accelerating Transformer Pre-training with 2:4 Sparsity"
collection: publications
permalink: /publication/accelerating-transformer-pre-t
excerpt: '"...this is the first report on end-to-end acceleration on pre-training transformers with 2:4 sparsity."'
date: 2024-07-21
venue: 'Forty-first International Conference on Machine Learning'
#slidesurl: 'http://academicpages.github.io/files/slides1.pdf'
paperurl: 'https://openreview.net/pdf?id=kTaX87Zn6M'
#citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---

***Yuezhou Hu, Kang Zhao, Weiyu Huang, Jianfei Chen, Jun Zhu*** Proceedings of the 41st International Conference on Machine Learning, PMLR 235:19531-19543, 2024.

**Abstract:**
Training large transformers is slow, but recent innovations on GPU architecture give us an advantage. NVIDIA Ampere GPUs can execute a fine-grained 2:4 sparse matrix multiplication twice as fast as its dense equivalent. In the light of this property, we comprehensively investigate the feasibility of accelerating feed-forward networks (FFNs) of transformers in pre-training. First, we define a ``flip rate'' to monitor the stability of a 2:4 training process. Utilizing this metric, we propose three techniques to preserve accuracy: to modify the sparse-refined straight-through estimator by applying the masked decay term on gradients, to determine a feasible decay factor in warm-up stage, and to enhance the model's quality by a dense fine-tuning procedure near the end of pre-training. Besides, we devise two techniques to practically accelerate training: to calculate transposable 2:4 masks by convolution, and to accelerate gated activation functions by reducing GPU L2 cache miss. Experiments show that our 2:4 sparse training algorithm achieves similar convergence to dense training algorithms on several transformer pre-training tasks, while actual acceleration can be observed on different shapes of transformer block apparently. Our toolkit is available at [https://github.com/huyz2023/2by4-pretrain](https://github.com/huyz2023/2by4-pretrain).