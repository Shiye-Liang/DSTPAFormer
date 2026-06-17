# DSTPFormer: Dynamic Spatial–Temporal Prior Learning for 3D Human Pose Estimation

## Abstract

Transformer and graph convolution-based methods have achieved remarkable progress in video-based 3D human pose estimation. However, existing approaches generally lack explicit constraints on human skeletal structure during feature fusion and make limited use of prior knowledge such as human kinematics and temporal motion continuity. To address these limitations, we propose a dual-branch Dynamic Spatiotemporal Prior-enhanced Transformer (DSTPFormer), which integrates the complementary strengths of GCNFormer and DPAFormer within a unified framework. Specifically, in the DPAFormer branch, we design two prior-aware attention modules: Spatial Prior Attention (SPA) and Temporal Prior Attention (TPA).SPA leverages human anatomical structure to guide spatial dependency modeling, while TPA exploits motion trajectory priors to enhance temporal feature learning. By embedding these priors into the multi-head self-attention mechanism, the proposed modules facilitate more effective modeling of long-range dependencies and discriminative pose representations. To further improve adaptability, we develop a Prior Adaptive Modulation (PAM) mechanism dynamically regulates and selectively enhances the contribution of prior knowledge.To strengthen cross-branch feature interaction, we propose a Structure-aware Dual-directional Cross Fusion (SDCF) module, which introduces a learnable skeletal graph structure between the graph convolution branch and the Transformer branches, thereby improving the structural consistency of pose prediction. Furthermore, the proposed SPA and TPA modules adopt a plug-and-play design, enabling seamless integration into various Transformer-based network architectures, including diffusion models, with minimal computational overhead. Extensive experiments on the Human3.6M and MPI-INF-3DHP benchmark datasets demonstrate that DSTPFormer consistently improves 3D human pose estimation performance and achieves state-of-the-art results under both diffusion-based and non-diffusion settings, validating the effectiveness of incorporating dynamic spatiotemporal priors and structure-aware feature fusion.

---

## Framework Overview

The overall architecture of DSTPFormer consists of three main stages:

1. **Feature Embedding**  
   Input 2D pose sequences are first embedded into high-dimensional feature representations.

2. **Dynamic Prior Learning Module**  
   Spatial and temporal priors are explicitly modeled and dynamically adjusted during training.

3. **Transformer-based Pose Decoder**  
   A Transformer backbone aggregates spatial-temporal dependencies and predicts 3D joint coordinates.

The model effectively integrates structural knowledge into attention learning, ensuring both spatial consistency and temporal smoothness.

---

## Key Components

### SPA and TPA (Spatial & Temporal Prior Attention)

- **SPA (Spatial Prior Attention)** models structural dependencies among human joints within each frame.
- **TPA (Temporal Prior Attention)** captures motion continuity across consecutive frames.
- Both modules introduce prior-guided attention to improve pose coherence and reduce ambiguity.

---

### PAM (Prior Aggregation Module)

The **PAM** module is designed to aggregate spatial and temporal priors into a unified representation. It adaptively fuses different prior signals, enabling the model to dynamically balance spatial structure and temporal dynamics.

---

### SDCF (Structure-aware Dynamic Cross Fusion)

The **SDCF** module performs cross-fusion between spatial and temporal branches:

- Explicitly encodes human kinematic constraints
- Enables bidirectional information exchange
- Enhances feature interaction between spatial and temporal streams
- Improves structural consistency of predicted poses

---

## To-Do List

- [ ] Release training code  
- [ ] Release pretrained models  
- [ ] Add detailed documentation  
- [ ] Provide installation guide  

---

## Installation

Coming soon.

---

## Training

Coming soon.

---

## Evaluation

Coming soon.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
