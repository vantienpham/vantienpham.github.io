---
layout: page
title: thesis
permalink: /thesis/
nav: true
nav_order: 4
show_title: false
---

<h2 align="center">
Deep Neural Network Compression Using <br> Pruning and Low-Rank Approximations
</h2>

<p align="center">
  <strong>Van Tien Pham</strong><br>
  Université de Toulon, CNRS, LIS (UMR 7020), France<br>
  Thesis period: 21/11/2022 – 28/11/2025
</p>

<hr>


### Abstract
<p style="text-align: justify;">
This thesis introduces five methods for neural network compression, focusing on pruning and low-rank approximations. First, <strong>CORING</strong> (effiCient tensOr decomposition-based filteR prunING) is an efficient pruning method that uses higher-order singular value decomposition to preserve the tensorial structure of convolutional filters, enabling effective low-rank approximations. Second, <strong>SLIMING</strong> (Singular vaLues-drIven autoMated filter prunING) is a singular value-driven framework that formulates pruning as a two-stage optimization problem, where both configuration and filter selection are guided by spectral properties. Third, <strong>NORTON</strong> (enhanced Network cOmpRession through TensOr decompositions and pruNing) is a hybrid approach that leverages the advantages of both tensor decomposition and structured pruning. Fourth, <strong>CoDeC</strong> (Coupled tensor Decomposition for Compact network representation) employs coupled canonical polyadic decomposition to jointly factorize groups of similar filters, with a custom similarity metric used for pre-clustering. Finally, <strong>Flex</strong> extends compression to matrix-valued multivariate functions through a decoupling framework formulated as a coupled matrix–tensor factorization problem, solved via alternating least squares with zeroth- and first-order information. Together, these contributions provide novel, mathematically grounded strategies to reduce model complexity while maintaining high performance across diverse neural architectures. Extensive experiments demonstrate consistent improvements over state-of-the-art methods in compression rate, accuracy, and computational efficiency. All methods are released as open-source repositories, facilitating reproducibility, industrial transfer, and community adoption.
</p>
**Keywords:** low-rank approximations, pruning, neural network compression


### Introduction
<p style="text-align: justify;">
Network compression is a key research area in machine learning and computer vision, aiming to reduce the computational and memory demands of deep neural networks while preserving their performance in tasks such as image recognition and interpretation. Its objective is to enable efficient deployment of high-performing models on resource-constrained platforms, including embedded and edge devices, while reducing inference latency and energy consumption.
</p>
<p style="text-align: justify;">
Despite significant progress, compressing deep neural networks remains a challenging problem due to several fundamental limitations of existing approaches. Many methods ignore the intrinsic multidimensional structure of network parameters, pruning strategies often rely on heuristics, tensor decompositions are usually applied independently per filter, and compression strategies are frequently architecture-dependent. Integrating multiple paradigms like pruning and tensor decomposition adds further complexity.
</p>
<p style="text-align: justify;">
This thesis proposes a coherent set of five contributions addressing these challenges, emphasizing preservation of multidimensional structure, reduction of heuristic design choices, and explicit modeling of redundancy. Together, the contributions explore structured pruning, tensor decomposition, and their integration in a unified framework, extending compression techniques to modern architectures like Transformers and MLP-Mixers. All methods are validated extensively and released as open-source.
</p>


### Contributions

#### CORING: Efficient Tensor Decomposition-Based Filter Pruning
[https://coring-ai.github.io/](https://coring-ai.github.io/)

- Introduces tensor decompositions (HOSVD) for filter pruning, preserving multidimensional structure while providing low-rank approximations.
- Enables versatile filter similarity calculations using HOSVD representations, avoiding full filters or reshaped versions.
- Efficient filter selection using similarity matrices and evaluation across diverse vision tasks demonstrating superior performance.

#### SLIMING: Singular Values-Driven Automated Filter Pruning
[https://sliming-ai.github.io/](https://sliming-ai.github.io/)

- Uses singular values to link filter redundancy with pruning optimization.
- Simplifies combinatorial complexity by dividing into configuration and selection problems with straightforward algorithms.
- Validated across 8 architectures, 4 datasets, and 4 vision tasks, compared with 58 existing pruning methods.

#### NORTON: Enhanced Network Compression Through Tensor Decompositions and Pruning
[https://norton-ai.github.io/](https://norton-ai.github.io/)

- Introduces filter decomposition, preserving multidimensional weight structure.
- Combines decomposition and pruning through a novel sequential scheme.
- Demonstrated superior performance across vision tasks compared to state-of-the-art.

#### CoDeC: Coupled Tensor Decomposition for Compact Network Representation
[https://codec-ai.github.io/](https://codec-ai.github.io/)

- Joint decomposition of similar filters via coupled CPD, reducing parameters and computational cost.
- Pre-clusters filters using a custom subspace-based distance metric.
- Validated on multiple architectures and tasks, outperforming existing methods.

#### Flex: Decoupling Matrix-Valued Functions Using Zeroth and First-Order Information
[https://flex-ai.github.io/](https://flex-ai.github.io/)


#### Tensor Decompositions for Signal Processing: Theory, Advances, and Applications
- Co–first author of survey paper analyzing tensor decomposition methods in signal processing and deep learning, with a focus on network compression.
- Authored section on neural network compression: theory, implementation, comparative evaluations, and open challenges.
- Maintains curated repository of tensor decomposition resources: [https://github.com/vantienpham/Awesome-Tensor-Decomposition](https://github.com/vantienpham/Awesome-Tensor-Decomposition)

---
