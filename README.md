# A Survey on NeRF and 3DGS for Aerial Scene Editing

[![Journal](https://img.shields.io/badge/Journal-The%20Visual%20Computer-blue)](https://www.springer.com/journal/371) 
[![arXiv](https://img.shields.io/badge/arXiv-24XX.XXXXX-b31b1b.svg)](https://arxiv.org/abs/your_paper_id) <!-- 提交arXiv后替换 'your_paper_id' -->

> This repository is the official resource collection for our survey paper:
> **"Implicit vs. Explicit: A Comparative Survey on NeRF and 3DGS for Large-Scale Aerial Scene Editing"**
>
> **Authors:** Rui Gong, Jiguang Zhang, Yujia Pang, Yixuan Wang, Xiaopeng Zhang, Weiliang Meng, and Peng Zhou.
>
> **Abstract:** *The proliferation of Unmanned Aerial Vehicles (UAVs) has significantly advanced the acquisition of large-scale 3D scene data, paving the way for applications like Digital Twins. Neural Radiance Fields (NeRF) and 3D Gaussian Splatting (3DGS) have enabled exceptional realism, yet editing these vast neural representations remains challenging. This survey provides a systematic analysis of large-scale scene editing from UAV aerial imagery, focusing on the fundamental architectural dichotomy between implicit (NeRF) and explicit (3DGS) representations. We introduce novel taxonomies, critically evaluate their core mechanisms, and reveal why explicit representations are converging as the more viable path for interactive, city-scale digital scene manipulation. Our analysis identifies key challenges and suggests future research directions.*
> 
> **To readers of our manuscript:** In this repository, we provide links to all the papers and datasets discussed. We kindly remind you that this resource is directly related to our manuscript currently under submission to *The Visual Computer*. **If you find our work and this collection useful, we encourage you to cite our survey.**

---

## 📖 Paper Collection based on Our Taxonomies

We categorize the surveyed papers according to the novel taxonomies proposed in our work. This structure directly corresponds to the analysis in our manuscript.

### **1. The Multimodal-driven NeRF Editing Pipeline**

As detailed in Section 2.1 of our survey, we deconstruct the NeRF editing process into a four-stage, optimization-based pipeline.

#### **1.1. Feature Extraction and Mapping**
*This stage translates abstract user intent into machine-interpretable formats using pre-trained models.*
- **CLIP-NeRF** (CVPR 2022) [[Paper]](https://arxiv.org/abs/2112.09081) [[Project]](https://cassie.style/clipnerf/) [[Code]](https://github.com/cassie-wang/CLIP-NeRF)
- **Text2NeRF** (TVCG 2024) [[Paper]](https://arxiv.org/abs/2303.12356) [[Code]](https://github.com/Jing-Li-2000/Text2NeRF)
- **Customize your NeRF** (arXiv 2023) [[Paper]](https://arxiv.org/abs/2307.03839)

#### **1.2. Conditional NeRF Architecture Design**
*This stage involves designing NeRF architectures that integrate semantic conditions to modulate scene geometry and appearance.*
- **CLIP-NeRF** (CVPR 2022) [[Paper]](https://arxiv.org/abs/2112.09081) [[Project]](https://cassie.style/clipnerf/) [[Code]](https://github.com/cassie-wang/CLIP-NeRF)
- **Text2NeRF** (TVCG 2024) [[Paper]](https://arxiv.org/abs/2303.12356) [[Code]](https://github.com/Jing-Li-2000/Text2NeRF)
- **Customize your NeRF** (arXiv 2023) [[Paper]](https://arxiv.org/abs/2307.03839)
- **MINE** (CVPR 2022) [[Paper]](https://arxiv.org/abs/2205.13459) [[Project]](https://lioryariv.github.io/mine/) [[Code]](https://github.com/lioryariv/mine)

#### **1.3. Targeted Optimization and Scene Update**
*This final stage adjusts the network’s weights to realize the desired edit, encompassing both forward and inverse optimization strategies.*
- **CLIP-NeRF** (Progressive Refinement) [[Paper]](https://arxiv.org/abs/2112.09081)
- **Text2NeRF** (Progressive Inpainting) [[Paper]](https://arxiv.org/abs/2303.12356)
- **Customize your NeRF** (Local-Global Iteration & Inverse Optimization) [[Paper]](https://arxiv.org/abs/2307.03839)
- **SinNeRF** (ECCV 2022) [[Paper]](https://arxiv.org/abs/2204.09312) [[Project]](https://dvl-tum.github.io/sin-nerf/) [[Code]](https://github.com/dvl-tum/sin-nerf)

---

### **2. The Interactive 3DGS Editing Workflow**

As introduced in Section 2.2 of our survey, we synthesize the 3DGS editing process into a five-stage, direct manipulation workflow.

#### **2.1. Initial Gaussian Layout Generation**
*This stage interprets user commands to generate an initial plan for the edit, defining its location, shape, and appearance.*
- **GaussianEditor** (CVPR 2024) [[Paper]](https://arxiv.org/abs/2311.12775) [[Project]](https://gauss-group.github.io/GaussianEditor/) [[Code]](https://github.com/Gauss-Group/GaussianEditor)
- **CG3D** (arXiv 2023) [[Paper]](https://arxiv.org/abs/2311.17907)
- **Align Your Gaussians** (CVPR 2024) [[Paper]](https://arxiv.org/abs/2312.02924) [[Project]](https://align-your-gaussians.github.io/)
- **GALA3D** (arXiv 2024) [[Paper]](https://arxiv.org/abs/2403.01873)
- **LangSplat** (CVPR 2024) [[Paper]](https://arxiv.org/abs/2403.13998) [[Project]](https://langsplat.github.io/) [[Code]](https://github.com/qi-feng/LangSplat)
- **GIR** (arXiv 2023) [[Paper]](https://arxiv.org/abs/2312.05133)

#### **2.2. 3D Gaussian Representation Construction**
*This stage explicitly defines new primitives by manipulating existing Gaussians (e.g., cloning, splitting).*
- **GaussianEditor** (CVPR 2024) [[Paper]](https://arxiv.org/abs/2311.12775)
- **LangSplat** (CVPR 2024) [[Paper]](https://arxiv.org/abs/2403.13998)
- **GaussianDreamer** (CVPR 2024) [[Paper]](https://arxiv.org/abs/2310.08529) [[Project]](https://taolei.sites.northeastern.edu/projects/gaussiandreamer/) [[Code]](https://github.com/hustvl/GaussianDreamer)
- **SC-GS** (arXiv 2024) [[Paper]](https://arxiv.org/abs/2403.01358) [[Project]](https://y-u-j-i-n.github.io/sc-gs/) [[Code]](https://github.com/y-u-j-i-n/SC-GS)
- **GIR** (arXiv 2023) [[Paper]](https://arxiv.org/abs/2312.05133)

#### **2.3. Geometric Optimization**
*This stage refines the core parameters of primitives (position, rotation, scale) to ensure structural coherence.*
- **GALA3D** (arXiv 2024) [[Paper]](https://arxiv.org/abs/2403.01873)
- **GSGEN** (ICLR 2024) [[Paper]](https://arxiv.org/abs/2311.15224) [[Project]](https://gsgen-3d.github.io/) [[Code]](https://github.com/gsgen-3d/gsgen)
- **GIR** (arXiv 2023) [[Paper]](https://arxiv.org/abs/2312.05133)
- **LangSplat** (CVPR 2024) [[Paper]](https://arxiv.org/abs/2403.13998)

#### **2.4. Surface Detail Enhancement**
*This stage focuses on appearance, encoding attributes like color, materials, and illumination for photorealism.*
- **GSGEN** (ICLR 2024) [[Paper]](https://arxiv.org/abs/2311.15224)
- **GaussianEditor** (CVPR 2024) [[Paper]](https://arxiv.org/abs/2311.12775)
- **GAvatar** (CVPR 2024) [[Paper]](https://arxiv.org/abs/2312.06732) [[Project]](https://ye-y.github.io/GAvatar/) [[Code]](https://github.com/ye-y/GAvatar)
- **LangSplat** (CVPR 2024) [[Paper]](https://arxiv.org/abs/2403.13998)
- **Text-to-3D Generation: A Survey** (includes many models like DreamFusion, Magic3D etc.) [[Paper]](https://arxiv.org/abs/2309.11416)
- **GALA3D** (arXiv 2024) [[Paper]](https://arxiv.org/abs/2403.01873)
- **GIR** (arXiv 2023) [[Paper]](https://arxiv.org/abs/2312.05133)

#### **2.5. Temporal Change and Dynamic Scene Support**
*This stage extends the model to handle time-varying events and motion.*
- **Efficient4D** (arXiv 2024) [[Paper]](https://arxiv.org/abs/2401.08742)
- **SC-GS** (arXiv 2024) [[Paper]](https://arxiv.org/abs/2403.01358)
- **Align Your Gaussians** (CVPR 2024) [[Paper]](https://arxiv.org/abs/2312.02924)
- **Human Gaussian Splatting** (arXiv 2023) [[Paper]](https://arxiv.org/abs/2311.10097) [[Project]](https://shunsukesaito.github.io/hugs/)

---

## 💾 Datasets for Scene Reconstruction & Editing

A summary of datasets discussed in our survey (corresponding to Table 1 in the manuscript), highlighting their relevance and limitations for the task of large-scale aerial scene editing.

| Dataset Name | Category | Description & Usage | Limitations for Aerial Scene Editing | Link |
| :--- | :--- | :--- | :--- | :--- |
| **NeRF-Synthetic** | Foundational | Synthetic objects with 360° views for validating NeRF models. | Lack of Realism & Scale. | [[Project]](https://www.matthewtancik.com/nerf) |
| **LLFF** | Foundational | Real-world, forward-facing scenes for view synthesis benchmarks. | Limited Viewpoint Coverage; small scale. | [[Project]](https://bmild.github.io/llff/) |
| **ScanNet** | Indoor | Large-scale RGB-D dataset of indoor scenes with rich annotations. | Indoor & Mesh-Based; goals differ from neural rendering. | [[Project]](http://www.scan-net.org/) |
| **UrbanScene3D** | Large-Scale Static | High-resolution UAV imagery of San Francisco for urban NeRFs. | Static & Unannotated; lacks labels for semantic edits. | [[Homepage]](https://vlar-group.github.io/UrbanScene3D/) |
| **Tanks and Temples** | Large-Scale Static | High-quality video for benchmarking MVS and photogrammetry. | No Ground-Truth Edits; for reconstruction, not modification. | [[Homepage]](https://www.tanksandtemples.org/) |
| **D-NeRF Dataset** | Dynamic Scenes | Synthetic video of objects with non-rigid motion. | Synthetic & Object-Scale; not representative of urban dynamics. | [[Project]](https://www.albertpumarola.com/d-nerf) |
| **Waymo Open / KITTI-360**| Autonomous Driving | Massive LiDAR/camera datasets with rich semantic labels. | Ground-Level Perspective; geometry and appearance differ significantly. | [[Waymo]](https://waymo.com/open/) [[KITTI-360]](http://www.cvlibs.net/datasets/kitti-360/) |

---

## 🚀 Future Research Directions

Our survey identifies several key areas for future innovation. We encourage the community to explore:
1.  **Unified and Hybrid Representations**: Moving beyond the implicit-explicit dichotomy.
2.  **Scalability and Efficiency**: For true city-scale, interactive models.
3.  **Physics-Informed and Physically Plausible Editing**: Integrating physical laws into the editing process.
4.  **Robust Multimodal Data Fusion**: Seamlessly fusing with GIS, LiDAR, and other data sources.
5.  **Intuitive Human-Computer Interaction Paradigms**: Developing more sophisticated HCI beyond text prompts.

## 🤝 Contribution

This is an active repository. If you have suggestions for adding new papers, datasets, or correcting information, please feel free to **open an issue** or **submit a pull request**. Let's build a comprehensive resource for the community together!

---

### **How to Cite**

```bibtex
@article{Gong2025Survey,
  title   = {Implicit vs. Explicit: A Comparative Survey on NeRF and 3DGS for Large-Scale Aerial Scene Editing},
  author  = {Gong, Rui and Zhang, Jiguang and Pang, Yujia and Wang, Yixuan and Zhang, Xiaopeng and Meng, Weiliang and Zhou, Peng},
  journal = {The Visual Computer},
  year    = {2025}
  % Note: Full citation details will be updated upon publication.
}
