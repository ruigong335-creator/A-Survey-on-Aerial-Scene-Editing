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
- **CLIP-NeRF** (CVPR 2022) [[Paper]](https://openaccess.thecvf.com/content/CVPR2022/papers/Wang_CLIP-NeRF_Text-and-Image_Driven_Manipulation_of_Neural_Radiance_Fields_CVPR_2022_paper.pdf) [[Code]](https://github.com/cassiePython/CLIPNeRF)
- **Text2NeRF** (TVCG 2024) [[Paper]](https://ieeexplore.ieee.org/abstract/document/10422989) [[Code]](https://github.com/eckertzhang/Text2NeRF)
- **Customize your NeRF** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/He_Customize_your_NeRF_Adaptive_Source_Driven_3D_Scene_Editing_via_CVPR_2024_paper.html) [[Code]](https://github.com/hrz2000/CustomNeRF)

#### **1.2. Conditional NeRF Architecture Design**
*This stage involves designing NeRF architectures that integrate semantic conditions to modulate scene geometry and appearance.*
- **CLIP-NeRF** (CVPR 2022) [[Paper]](https://openaccess.thecvf.com/content/CVPR2022/papers/Wang_CLIP-NeRF_Text-and-Image_Driven_Manipulation_of_Neural_Radiance_Fields_CVPR_2022_paper.pdf) [[Code]](https://github.com/cassiePython/CLIPNeRF)
- **Text2NeRF** (TVCG 2024) [[Paper]](https://ieeexplore.ieee.org/abstract/document/10422989) [[Code]](https://github.com/eckertzhang/Text2NeRF)
- **Customize your NeRF** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/He_Customize_your_NeRF_Adaptive_Source_Driven_3D_Scene_Editing_via_CVPR_2024_paper.html) [[Code]](https://github.com/hrz2000/CustomNeRF)
- **MINE** (ICCV 2021) [[Paper]](https://openaccess.thecvf.com/content/ICCV2021/html/Li_MINE_Towards_Continuous_Depth_MPI_With_NeRF_for_Novel_View_ICCV_2021_paper.html) [[Code]](https://github.com/vincentfung13/MINE)

#### **1.3. Targeted Optimization and Scene Update**
*This final stage adjusts the network’s weights to realize the desired edit, encompassing both forward and inverse optimization strategies.*
- **CLIP-NeRF** (Progressive Refinement) [[Paper]](https://openaccess.thecvf.com/content/CVPR2022/papers/Wang_CLIP-NeRF_Text-and-Image_Driven_Manipulation_of_Neural_Radiance_Fields_CVPR_2022_paper.pdf)
- **Text2NeRF** (Progressive Inpainting) [[Paper]](https://ieeexplore.ieee.org/abstract/document/10422989)
- **Customize your NeRF** (Local-Global Iteration & Inverse Optimization) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/He_Customize_your_NeRF_Adaptive_Source_Driven_3D_Scene_Editing_via_CVPR_2024_paper.html)
- **SinNeRF** (ECCV 2022) [[Paper]](https://link.springer.com/chapter/10.1007/978-3-031-20047-2_42) [[Code]](https://github.com/VITA-Group/SinNeRF)

---

### **2. The Interactive 3DGS Editing Workflow**

As introduced in Section 2.2 of our survey, we synthesize the 3DGS editing process into a five-stage, direct manipulation workflow.

#### **2.1. Initial Gaussian Layout Generation**
*This stage interprets user commands to generate an initial plan for the edit, defining its location, shape, and appearance.*
- **GaussianEditor** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Chen_GaussianEditor_Swift_and_Controllable_3D_Editing_with_Gaussian_Splatting_CVPR_2024_paper.html) [[Code]](https://github.com/buaacyw/GaussianEditor)
- **CG3D** (arXiv 2023) [[Paper]](https://arxiv.org/abs/2311.17907) [[Code]](https://github.com/asvilesov/CG3D)
- **Align Your Gaussians** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Ling_Align_Your_Gaussians_Text-to-4D_with_Dynamic_3D_Gaussians_and_Composed_CVPR_2024_paper.html)
- **GALA3D** (arXiv 2024) [[Paper]](https://arxiv.org/abs/2412.20473)
- **LangSplat** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Qin_LangSplat_3D_Language_Gaussian_Splatting_CVPR_2024_paper.html) [[Code]](https://github.com/minghanqin/LangSplat)
- **GIR** (IEEE VR 2024) [[Paper]](https://ieeexplore.ieee.org/abstract/document/11030850) [[Code]](https://github.com/guduxiaolang/GIR)

#### **2.2. 3D Gaussian Representation Construction**
*This stage explicitly defines new primitives by manipulating existing Gaussians (e.g., cloning, splitting).*
- **GaussianEditor** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Chen_GaussianEditor_Swift_and_Controllable_3D_Editing_with_Gaussian_Splatting_CVPR_2024_paper.html) [[Code]](https://github.com/buaacyw/GaussianEditor)
- **LangSplat** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Qin_LangSplat_3D_Language_Gaussian_Splatting_CVPR_2024_paper.html) [[Code]](https://github.com/minghanqin/LangSplat)
- **GaussianDreamer** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Yi_GaussianDreamer_Fast_Generation_from_Text_to_3D_Gaussians_by_Bridging_CVPR_2024_paper.html) [[Code]](https://github.com/hustvl/GaussianDreamer)
- **SC-GS** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Huang_SC-GS_Sparse-Controlled_Gaussian_Splatting_for_Editable_Dynamic_Scenes_CVPR_2024_paper.html) [[Code]](https://github.com/CVMI-Lab/SC-GS)
- **GIR** (IEEE VR 2024) [[Paper]](https://ieeexplore.ieee.org/abstract/document/11030850) [[Code]](https://github.com/guduxiaolang/GIR)

#### **2.3. Geometric Optimization**
*This stage refines the core parameters of primitives (position, rotation, scale) to ensure structural coherence.*
- **GALA3D** (arXiv 2024) [[Paper]](https://arxiv.org/abs/2412.20473)
- **GSGEN** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Chen_Text-to-3D_using_Gaussian_Splatting_CVPR_2024_paper.html) [[Code]](https://github.com/gsgen3d/gsgen)
- **GIR** (IEEE VR 2024) [[Paper]](https://ieeexplore.ieee.org/abstract/document/11030850) [[Code]](https://github.com/guduxiaolang/GIR)
- **LangSplat** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Qin_LangSplat_3D_Language_Gaussian_Splatting_CVPR_2024_paper.html) [[Code]](https://github.com/minghanqin/LangSplat)

#### **2.4. Surface Detail Enhancement**
*This stage focuses on appearance, encoding attributes like color, materials, and illumination for photorealism.*
- **GSGEN** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Chen_Text-to-3D_using_Gaussian_Splatting_CVPR_2024_paper.html) [[Code]](https://github.com/gsgen3d/gsgen)
- **GaussianEditor** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Chen_GaussianEditor_Swift_and_Controllable_3D_Editing_with_Gaussian_Splatting_CVPR_2024_paper.html) [[Code]](https://github.com/buaacyw/GaussianEditor)
- **GAvatar** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Yuan_GAvatar_Animatable_3D_Gaussian_Avatars_with_Implicit_Mesh_Learning_CVPR_2024_paper.html)
- **LangSplat** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Qin_LangSplat_3D_Language_Gaussian_Splatting_CVPR_2024_paper.html) [[Code]](https://github.com/minghanqin/LangSplat)
- **GALA3D** (arXiv 2024) [[Paper]](https://arxiv.org/abs/2412.20473)
- **GIR** (IEEE VR 2024) [[Paper]](https://ieeexplore.ieee.org/abstract/document/11030850) [[Code]](https://github.com/guduxiaolang/GIR)

#### **2.5. Temporal Change and Dynamic Scene Support**
*This stage extends the model to handle time-varying events and motion.*
- **Efficient4D** (arXiv 2024) [[Paper]](https://arxiv.org/abs/2401.08742) [[Code]](https://github.com/fudan-zvg/Efficient4D)
- **SC-GS** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Huang_SC-GS_Sparse-Controlled_Gaussian_Splatting_for_Editable_Dynamic_Scenes_CVPR_2024_paper.html) [[Code]](https://github.com/CVMI-Lab/SC-GS)
- **Align Your Gaussians** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Ling_Align_Your_Gaussians_Text-to-4D_with_Dynamic_3D_Gaussians_and_Composed_CVPR_2024_paper.html)
- **Human Gaussian Splats** (CVPR 2024) [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Kocabas_HUGS_Human_Gaussian_Splats_CVPR_2024_paper.html) [[Code]](https://github.com/apple/ml-hugs)

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
