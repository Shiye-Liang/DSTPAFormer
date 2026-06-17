# DSTPFormer: Dynamic Spatial–Temporal Prior Learning for 3D Human Pose Estimation

## Abstract

**DSTPFormer** is a novel Transformer-based framework for monocular 3D human pose estimation from videos. The key idea is to explicitly model **dynamic spatial and temporal priors** to enhance the structural consistency and motion coherence of human poses.

Unlike previous methods that rely purely on data-driven attention mechanisms, DSTPFormer introduces a **prior-aware learning paradigm** that integrates spatial and temporal structural constraints into the Transformer architecture. This enables more robust modeling of joint dependencies and long-term motion dynamics, leading to improved performance in challenging real-world scenarios.

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
