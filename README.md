# awesome-Implicit-NeRF-SLAM [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

This repo contains a curative list of **Implicit Representations and NeRF papers relating to SLAM/Robotics domain**, inspired by [Awesome-Implicit-NeRF-Robotics](https://github.com/zubair-irshad/Awesome-Implicit-NeRF-Robotics) <br>

#### Please feel free to send me [pull requests](https://github.com/DoongLi/awesome-Implicit-NeRF-SLAM/blob/main/how-to-PR.md) or [email](mailto:lidong8421bcd@gmail.com) to add papers! <br>

If you find this repository useful, please consider [citing](#citation) and STARing this list. Feel free to share this list with others!

For an overview of **NeRFs**, checkout the Survey ([Neural Volume Rendering: NeRF And Beyond](https://arxiv.org/abs/2101.05204) and [NeRF: Neural Radiance Field in 3D Vision, A Comprehensive Review](https://arxiv.org/pdf/2210.00379.pdf)), Blog post ([NeRF Explosion 2020](https://dellaert.github.io/NeRF/)) and Collection ([awesome-NeRF](https://github.com/yenchenlin/awesome-NeRF))

---

## Overview

  - [NeRF General Model](#nerf-general-model)

  - [SLAM](#slam)
    - [Visual-SLAM](#Visual-SLAM)
    - [Lidar-SLAM](#Lidar-SLAM)
    - [Multimodal-SLAM](#Multimodal-SLAM)

  - [Robotics](#Robotics)

    - [Manipulation/RL](#manipulationrl)

    - [Planning/Navigation](#planningnavigation)

    - [Localization](#localization)

  - [Citation](#citation)

---

## NeRF General Model

- **NeRF**: Representing Scenes as Neural Radiance Fields for View Synthesis, *ECCV, 2020*. [[Paper](https://arxiv.org/pdf/2003.08934.pdf)] [[Tensorflow Code](https://github.com/bmild/nerf)] [[Webpage](http://tancik.com/nerf)] [[Video](https://www.youtube.com/watch?v=JuH79E8rdKc)] 

* **ShAPO**: Implicit Representations for Multi Object Shape Appearance and Pose Optimization, *ECCV, 2022*. [[Paper](https://arxiv.org/pdf/2207.13691.pdf)] [[Pytorch Code](https://github.com/zubair-irshad/shapo)] [[Webpage](https://zubair-irshad.github.io/projects/ShAPO.html)] [[Video](https://youtu.be/LMg7NDcLDcA)] 
* **NCF**: Neural Correspondence Field for Object Pose Estimation, *ECCV, 2022*. [[Paper](https://arxiv.org/pdf/2208.00113.pdf)] [[Pytorch Code]( https://github.com/LinHuang17/NCF-code)] [[Webpage](https://linhuang17.github.io/NCF/)]
* **Neural-Sim**: Learning to Generate Training Data with NeRF, *ECCV 2022*.  [[Paper](https://arxiv.org/pdf/2207.11368.pdf)] [[Pytorch Code](https://github.com/gyhandy/Neural-Sim-NeRF)] [[Webpage](https://fylwen.github.io/disp6d.html)]
* **SNAKE**: SNAKE: Shape-aware Neural 3D Keypoint Field, *NeurIPS, 2022*. [[Paper](https://arxiv.org/abs/2206.01724.pdf)] [[Pytorch Code](https://github.com/zhongcl-thu/SNAKE)]
* **NeRF-RPN**: A general framework for object detection in NeRFs, *arXiv, 2022*. [[Paper](https://arxiv.org/abs/2211.11646)] [[Video](https://youtu.be/M8_4Ih1CJjE)] 
* **nerf2nerf**: Pairwise Registration of Neural Radiance Fields, *ICRA, 2023*.  [[Paper](https://arxiv.org/pdf/2211.01600.pdf)] [[Pytorch Code]( https://github.com/nerf2nerf/nerf2nerf)] [[Webpage](https://nerf2nerf.github.io/)] [[Dataset](https://drive.google.com/drive/folders/1jNpwAv1T1ntjIHUMJ1wABePA2Z8_nRRQ)]
* **iNeRF**: Inverting Neural Radiance Fields for Pose Estimation, *IROS, 2021*. [[Paper](https://arxiv.org/pdf/2012.05877.pdf)] [[Pytorch Code](https://github.com/yenchenlin/iNeRF-public)] [[Website](https://yenchenlin.me/inerf/)] [[Dataset](https://github.com/BerkeleyAutomation/dex-nerf-datasets)]
* **Point-NeRF**: Point-based Neural Radiance Fields, *CVPR, 2022*. [[Paper](https://arxiv.org/pdf/2201.08845.pdf)] [[Pytorch Code](https://github.com/Xharlie/pointnerf)] [[Website](https://xharlie.github.io/projects/project_sites/pointnerf/)]
* **Zip-NeRF**: Anti-Aliased Grid-Based Neural Radiance Fields, *ICCV, 2023*. [[Paper](https://arxiv.org/abs/2304.06706)] [[Website](https://jonbarron.info/zipnerf/)] [[Video](https://www.youtube.com/watch?v=xrrhynRzC8k)]
* **Mip-NeRF 360**: Unbounded Anti-Aliased Neural Radiance Fields, *CVPR, 2022*. [[Paper](https://arxiv.org/abs/2111.12077)] [[JAX Code]( https://github.com/google-research/multinerf)] [[Website](https://jonbarron.info/mipnerf360/)] [[Dataset](http://storage.googleapis.com/gresearch/refraw360/360_v2.zip)] [[Video](https://www.youtube.com/watch?v=zBSH-k9GbV4&feature=youtu.be)]
* **F2-NeRF**: Fast Neural Radiance Field Training with Free Camera Trajectories, *CVPR, 2023*. [[Paper](https://arxiv.org/pdf/2303.15951.pdf)] [[Pytorch Code](https://github.com/totoro97/f2-nerf)] [[Website](https://totoro97.github.io/projects/f2-nerf/)] [[Dataset](https://www.dropbox.com/sh/jmfao2c4dp9usji/AAC7Ydj6rrrhy1-VvlAVjyE_a?dl=0)]
* 3D Gaussian Splatting for Real-Time Radiance Field Rendering, *SIGGRAPH, 2023*. [[Paper](https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/3d_gaussian_splatting_low.pdf)] [[Website](https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/)]
* 2D Gaussian Splatting for Geometrically Accurate Radiance Fields, *SIGGRAPH, 2024*. [[Paper](https://arxiv.org/pdf/2403.17888)] [[Website](https://surfsplatting.github.io/)]  [[Code](https://github.com/hbb1/2d-gaussian-splatting)]

---

## SLAM

### Survey Paper
- How NeRFs and 3D Gaussian Splatting are Reshaping SLAM: a Survey, *arXiv, 2024*.[[Paper](https://arxiv.org/pdf/2402.13255.pdf)]
- SLAM Meets NeRF: A Survey of Implicit SLAM Methods, *World Electric Vehicle Journal, 2024*. [[Paper](https://www.mdpi.com/2032-6653/15/3/85)]
- NeRF in Robotics: A Survey, *arXiv, 2024*.[[Paper](https://arxiv.org/pdf/2405.01333)]

### Benchmarks
- Customizable Perturbation Synthesis for Robust SLAM Benchmarking, *arXiv, 2024*.[[Paper](https://arxiv.org/pdf/2402.08125.pdf)]
- Benchmarking Implicit Neural Representation and Geometric Rendering in Real-Time RGB-D SLAM, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2403.19473.pdf)] [[Code](https://github.com/thua919/NeRF-SLAM-Benchmark-CVPR24)] [[Website](https://vlis2022.github.io/nerf-slam-benchmark/)]
- Benchmarking Neural Radiance Fields for Autonomous Robots: An Overview, *arXiv, 2024*.[[Paper](https://arxiv.org/pdf/2405.05526)]
- From Perfect to Noisy World Simulation: Customizable Embodied Multi-modal Perturbations for SLAM Robustness Benchmarking, *arXiv, 2024*.[[Paper](https://arxiv.org/pdf/2406.16850)] [[Code](https://github.com/Xiaohao-Xu/SLAM-under-Perturbation)]

### Visual-SLAM

- **NeuralRecon**: Real-Time Coherent 3D Reconstruction from Monocular Video, *CVPR, 2021*.[[Paper](https://arxiv.org/pdf/2104.00681.pdf)] [[Pytorch Code](https://github.com/zju3dv/NeuralRecon/)] [[Website](https://zju3dv.github.io/neuralrecon/)]

- **Di-fusion**: Online implicit 3d reconstruction with deep priors, *CVPR, 2021*.[[Paper](https://openaccess.thecvf.com/content/CVPR2021/papers/Huang_DI-Fusion_Online_Implicit_3D_Reconstruction_With_Deep_Priors_CVPR_2021_paper.pdf)] [[Pytorch Code](https://github.com/huangjh-pub/di-fusion)] 

* **iSDF**: Real-Time Neural Signed Distance Fields for Robot Perception, *RSS, 2022*. [[Paper](https://arxiv.org/abs/2204.02296)] [[Pytorch Code](https://github.com/facebookresearch/iSDF)] [[Website](https://joeaortiz.github.io/iSDF/)]
* **LENS**: LENS: Localization enhanced by NeRF synthesis, *CoRL, 2021*. [[Paper](https://arxiv.org/abs/2110.06558)] [[Video](https://www.youtube.com/watch?v=DgIpVoS6ejY)] 
* **NICE-SLAM**: Neural Implicit Scalable Encoding for SLAM, *CVPR, 2021*. [[Paper](https://arxiv.org/abs/2112.12130)] [[Pytorch Code](https://github.com/cvg/nice-slam)] [[Website](https://pengsongyou.github.io/nice-slam?utm_source=catalyzex.com)]
* **iMAP**: Implicit Mapping and Positioning in Real-Time, *ICCV, 2021*. [[Paper](https://arxiv.org/abs/2103.12352)] [[Website](https://edgarsucar.github.io/iMAP/)] [[Video](https://www.youtube.com/watch?v=c-zkKGArl5Y)] 
* **BNV-Fusion**: BNV-Fusion: Dense 3D Reconstruction using Bi-level Neural Volume Fusion, *CVPR, 2022*. [[Paper](https://arxiv.org/pdf/2204.01139.pdf)] [[Pytorch Code](https://github.com/likojack/bnv_fusion)]
* **NeRF-SLAM**: Real-Time Dense Monocular SLAM with Neural Radiance Fields, *IROS, 2023*. [[Paper](https://arxiv.org/pdf/2210.13641.pdf)] [[Pytorch Code](https://github.com/ToniRV/NeRF-SLAM)] [[Video](https://www.youtube.com/watch?v=-6ufRJugcEU)]
* **Nerfels**: Renderable Neural Codes for Improved Camera Pose Estimation, *CVPR 2022 Workshop*. [[Paper](https://openaccess.thecvf.com/content/CVPR2022W/IMW/papers/Avraham_Nerfels_Renderable_Neural_Codes_for_Improved_Camera_Pose_Estimation_CVPRW_2022_paper.pdf)]
* SDF-based RGB-D Camera Tracking in Neural Scene Representations, *ICRA Workshop, 2022*. [[Paper](https://neural-implicit-workshop.stanford.edu/assets/pdf/bruns.pdf)]
* **Orbeez-SLAM**: A Real-time Monocular Visual SLAM with ORB Features and NeRF-realized Mapping, *ICRA, 2023*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10160950)] [[Video](https://www.youtube.com/watch?v=uzb-tVcPETE)] [[Code](https://github.com/MarvinChung/Orbeez-SLAM)]
* **ESLAM**: Efficient Dense SLAM System Based on Hybrid Representation of Signed Distance Fields, *CVPR,  2023*. [[Paper](https://arxiv.org/pdf/2211.11704.pdf)]
* **Vox-Fusion**: Dense Tracking and Mapping with Voxel-based Neural Implicit Representation, *ISMAR,  2022*. [[Paper](https://arxiv.org/pdf/2210.15858.pdf)] [[Website](https://yangxingrui.com/vox-fusion/)] [[Pytorch Code](https://github.com/zju3dv/Vox-Fusion)] [[Video](https://www.youtube.com/watch?v=Prp28y1b2Qs)]
* Visual-Inertial Odometry Priors for Bundle-Adjusting Neural Radiance Fields, *ICCAS, 2022*. [[Paper](http://mpil.sookmyung.ac.kr/wp-content/uploads/2022/12/2022_ICCAS_Kim.pdf)]
* Feature-Realistic Neural Fusion for Real-Time, Open Set Scene Understanding, *ICRA,  2022*. [[Paper](https://arxiv.org/pdf/2210.03043.pdf)]  [[Website](https://yangxingrui.com/vox-fusion/)] [[Video](https://www.youtube.com/watch?v=ysaohKI_Pf0)]
* Towards Open World NeRF-Based SLAM, *CRV, 2023*.  [[Paper](https://arxiv.org/pdf/2301.03102.pdf)]
* Dense RGB SLAM with Neural Implicit Maps, *ICLR, 2023*. [[Paper](https://arxiv.org/pdf/2301.08930v1.pdf)] [[Website](https://poptree.github.io/DIM-SLAM/)] [[Code](https://github.com/HKUST-3DV/DIM-SLAM)] [[Video]()]
* **vMAP**: Vectorised Object Mapping for Neural Field SLAM, *CVPR,  2023*. [[Paper](https://arxiv.org/pdf/2302.01838.pdf)] [[Website](https://kxhit.github.io/vMAP)] [[Pytorch Code](https://github.com/kxhit/vMAP)] [[Video](https://kxhit.github.io/media/vMAP/vmap_raw.mp4)]
* **NICER-SLAM**: Neural Implicit Scene Encoding for RGB SLAM, *3DV 2024*. [[Paper](https://arxiv.org/pdf/2302.03594.pdf)] [[Video](https://www.youtube.com/watch?v=tUXzqEZWg2w)]
* Implicit Map Augmentation for Relocalization, *ECCV Workshop, 2022*. [[Paper](https://link.springer.com/chapter/10.1007/978-3-031-25066-8_36)]
* **Uni-Fusion**: Universal Continuous Mapping, *TRO, 2023*.[[Paper](https://arxiv.org/pdf/2303.12678.pdf)] [[Code](https://github.com/Jarrome/Uni-Fusion)] [[Website](https://jarrome.github.io/Uni-Fusion/)]
* **NEWTON**: Neural View-Centric Mapping for On-the-Fly Large-Scale SLAM, *RAL, 2024*. [[Paper](https://arxiv.org/pdf/2303.13654v1.pdf)]
* **Point-SLAM**: Dense Neural Point Cloud-based SLAM, *ICCV, 2023*. [[Paper](https://arxiv.org/pdf/2304.04278.pdf)] [[Code](https://github.com/tfy14esa/Point-SLAM)]
* **RO-MAP**: Real-Time Multi-Object Mapping with Neural Radiance Fields, *RAL, 2023*. [[Paper](https://ieeexplore.ieee.org/document/10209177)] [[Code](https://github.com/XiaoHan-Git/RO-MAP)] [[Video](https://www.youtube.com/watch?v=sFrLXPw40wU)]
* **Co-SLAM**: Joint Coordinate and Sparse Parametric Encodings for Neural Real-Time SLAM, *CVPR, 2023*. [[Paper](https://arxiv.org/pdf/2304.14377.pdf)] [[Website](https://hengyiwang.github.io/projects/CoSLAM)]
* Neural Implicit Dense Semantic SLAM, *arXiv, 2023*. [[Paper](https://arxiv.org/pdf/2304.14560.pdf)]
* **FMapping**: Factorized Efficient Neural Field Mapping for Real-Time Dense RGB SLAM, *arXiv, 2023*. [[Paper](https://arxiv.org/pdf/2306.00579v1.pdf)] [[Website](https://vlis2022.github.io/fmap/)] [[Code](https://github.com/thua919/FMapping)] 
* **UncLe-SLAM**: Uncertainty Learning for Dense Neural SLAM, *arXiv, 2023*. [[Paper](https://arxiv.org/pdf/2306.11048.pdf)]
* **iMODE**:Real-Time Incremental Monocular Dense Mapping Using Neural Field, *ICRA, 2023*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10161538)]
* **NISB-Map**: Scalable Mapping With Neural Implicit Spatial Block, *RAL, 2023*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10163242)]
* RGB-D Mapping and Tracking in a Plenoxel Radiance Field, *WACV, 2024*. [[Paper](https://arxiv.org/pdf/2307.03404.pdf)]
* Efficient Map Fusion for Multiple Implicit SLAM Agents, *TIV, 2023*. [[Paper](https://ieeexplore.ieee.org/abstract/document/10189088)]
* **MIPS-Fusion**: Multi-Implicit-Submaps for Scalable and Robust Online Neural RGB-D Reconstruction, *TOG, 2023*. [[Paper](https://arxiv.org/pdf/2308.08741.pdf)]
* **GO-SLAM**: Global Optimization for Consistent 3D Instant Reconstruction, *ICCV, 2023*. [[Paper](https://arxiv.org/pdf/2309.02436.pdf)] [[Website](https://youmi-zym.github.io/projects/GO-SLAM/)] [[Code](https://github.com/youmi-zym/GO-SLAM)] 
* End-to-End RGB-D SLAM with Multi-MLPs Dense Neural Implicit Representations, *RAL, 2023*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10238793)]
* **DynaMoN**: Motion-Aware Fast And Robust Camera Localization for Dynamic NeRF, *arXiv, 2023*. [[Paper](https://arxiv.org/pdf/2309.08927.pdf)]
* **HI-SLAM**: Monocular Real-time Dense Mapping with Hybrid Implicit Fields, *RAL, 2023*. [[Paper](https://arxiv.org/pdf/2310.04787.pdf)]
* **CP-SLAM**: Collaborative Neural Point-based SLAM, *NeurIPS, 2023*. [[Paper](https://openreview.net/pdf?id=dFSeZm6dTC)]
* Learning Neural Implicit through Volume Rendering with Attentive Depth Fusion Priors,  *NeurIPS, 2023*. [[Paper](https://arxiv.org/pdf/2310.11598.pdf)] [[Code](https://github.com/MachinePerceptionLab/Attentive_DFPrior)] [[Website](https://machineperceptionlab.github.io/Attentive_DF_Prior/)]
* **NGEL-SLAM**: Neural Implicit Representation-based Global Consistent Low-Latency SLAM System, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2311.09525.pdf)] [[Code](https://github.com/YunxuanMao/ngel_slam)] 
* **SNI-SLAM**: Semantic Neural Implicit SLAM, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2311.11016.pdf)] [[Code](https://github.com/IRMVLab/SNI-SLAM)]
* Implicit Event-RGBD Neural SLAM, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2311.11013.pdf)]
* **DNS SLAM**: Dense Neural Semantic-Informed SLAM, *arXiv, 2023*. [[Paper](https://arxiv.org/pdf/2312.00204.pdf)]
* **PLGSLAM**: Progressive Neural Scene Representation with Local to Global Bundle Adjustment, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2312.09866.pdf)]
* **NeRF-VO**: Real-Time Sparse Visual Odometry with Neural Radiance Fields, *RAL, 2024*. [[Paper](https://arxiv.org/pdf/2312.13471.pdf)]
* Ternary-type Opacity and Hybrid Odometry for RGB-only NeRF-SLAM, *arXiv, 2023*. [[Paper](https://arxiv.org/pdf/2312.13332.pdf)]
* **DN-SLAM**: A Visual SLAM with ORB Features and NeRF Mapping in Dynamic Environments, *Sensors, 2023*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10376402)]
* **NID-SLAM**: Neural Implicit Representation-based RGB-D SLAM in dynamic environments, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2401.01189.pdf)]
* **DDN-SLAM**: Real-time Dense Dynamic Neural Implicit SLAM with Joint Semantic Encoding, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2401.01545.pdf)] [[Code](https://github.com/DrLi-Ming/DDN-SLAM)]
* **Hi-Map**: Hierarchical Factorized Radiance Field for High-Fidelity Monocular Dense Mapping, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2401.03203.pdf)] [[Website](https://vlis2022.github.io/fmap/)] [[Code](https://github.com/thua919/FMapping)]
* **NeuV-SLAM**: Fast Neural Multiresolution Voxel Optimization for RGBD Dense SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2402.02020.pdf)] [[Code](https://github.com/DARYL-GWZ/NeuV-SLAM)]
* **Structerf-SLAM**: Neural implicit representation SLAM for structural environments, *Computers & Graphics, 2024*. [[Paper](https://www.sciencedirect.com/science/article/abs/pii/S0097849324000207)]
* **Loopy-SLAM**: Dense Neural SLAM with Loop Closures, *CVPR, 2024*. [[Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Liso_Loopy-SLAM_Dense_Neural_SLAM_with_Loop_Closures_CVPR_2024_paper.pdf)] [[Code](https://github.com/eriksandstroem/Loopy-SLAM)] [[Website](https://notchla.github.io/Loopy-SLAM/)]
* **Q-SLAM**: Quadric Representations for Monocular SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.08125.pdf)]
* **DVN-SLAM**: Dynamic Visual Neural SLAM Based on Local-Global Encoding, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.11776.pdf)]
* **H3-Mapping**: Quasi-Heterogeneous Feature Grids for Real-time Dense Mapping Using Hierarchical Hybrid Representation, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.10821.pdf)]
* **Vox-Fusion++**: Voxel-based Neural Implicit Dense Tracking and Mapping with Multi-maps, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.12536.pdf)] [[Code](https://github.com/zju3dv/Vox-Fusion_Plus_Plus)]
* **MUTE-SLAM**: Real-Time Neural SLAM with Multiple Tri-Plane Hash Representations, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.17765.pdf)]
* **GlORIE-SLAM**: Globally Optimized RGB-only Implicit Encoding Point Cloud SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.19549.pdf)]
* Efficient 3D Instance Mapping and Localization with Neural Fields, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.19797.pdf)] [[Website](https://gtangg12.github.io/iML/)]
* **NeSLAM**: Neural Implicit Mapping and Self-Supervised Feature Tracking With Depth Completion and Denoising, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.20034.pdf)]
* **KN-SLAM**: Keypoints and Neural Implicit Encoding SLAM, *TIM, 2024*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10474286)]
* **SLAIM**: Robust Dense Neural SLAM for Online Tracking and Mapping, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2404.11419.pdf)]
* **EC-SLAM**: Real-time Dense Neural RGB-D SLAM System with Effectively Constrained Global Bundle Adjustment, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2404.13346.pdf)] [[Code](https://github.com/Lightingooo/EC-SLAM)]
* **S3-SLAM**: Sparse Tri-plane Encoding for Neural Implicit SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2404.18284)]
* **DF-SLAM**: Neural Feature Rendering Based on Dictionary Factors Representation for High-Fidelity Dense Visual SLAM System, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2404.17876)] [[Code](https://github.com/funcdecl/DF-SLAM)]
* Neural Graph Mapping for Dense SLAM with Efficient Loop Closure, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.03633)] [[Code](https://github.com/KTH-RPL/neural_graph_mapping)] [[Website](https://kth-rpl.github.io/neural_graph_mapping/)]
* **MGS-SLAM**: Monocular Sparse Tracking and Gaussian Mapping with Depth Smooth Regularization, *arXiv 2024*. [[Paper](https://arxiv.org/pdf/2405.06241)]
* **VPE-SLAM**: Neural Implicit Voxel-Permutohedral Encoding for SLAM, *ICRA, 2024*. [[Paper](todo)] [[Code](https://github.com/NeuCV-IRMI/VPE-SLAM)]
* **ONeK-SLAM**: A Robust Object-Level Dense SLAM Based on Joint Neural Radiance Fields and Keypoints, *ICRA 2024*. [[Paper](todo)]
* **HERO-SLAM**: Hybrid Enhanced Robust Optimization of Neural SLAM, *ICRA, 2024*. [[Paper](todo)] [[Code](https://github.com/hero-slam/HERO-SLAM)] [[Website](https://hero-slam.github.io/)]
* **NeB-SLAM**: Neural Blocks-based Salable RGB-D SLAM for Unknown Scenes, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.15151)]
* **ENeRF-SLAM**:A Dense Endoscopic SLAM With Neural Implicit Representation, *TMRB, 2024*. [[Paper](https://ieeexplore.ieee.org/abstract/document/10542414)] [[Code](https://github.com/Mar-lll/ENeRF-SLAM)]
* IBD-SLAM: Learning Image-Based Depth Fusion for Generalizable SLAM, *CVPR, 2024*. [[Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Yin_IBD-SLAM_Learning_Image-Based_Depth_Fusion_for_Generalizable_SLAM_CVPR_2024_paper.pdf)] [[Website](https://visual-ai.github.io/ibd-slam)]
* **RoDyn-SLAM**: Robust Dynamic Dense RGB-D SLAM with Neural Radiance Fields, *RAL, 2024*. [[Paper](https://arxiv.org/pdf/2407.01303)] [[Code](https://github.com/fudan-zvg/Rodyn-SLAM)]
* **MoD-SLAM**: Monocular Dense Mapping for Unbounded 3D Scene Reconstruction,  *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2402.03762.pdf)]
* Evaluating geometric accuracy of NeRF reconstructions compared to SLAM method,  *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2407.11238)]
* **I2-SLAM**: Inverting Imaging Process for Robust Photorealistic Dense SLAM,  *ECCV, 2024*. [[Paper](https://arxiv.org/abs/2407.11347v1)]
* An Artificial-Intelligence-based SLAM Processor with Scene-adaptive Sampling and Hybrid NeRF Model Training Acceleration,  *TCASAI, 2024*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10595406)]
---

### Lidar-SLAM

- **SHINE-Mapping**: Large-Scale 3D Mapping Using Sparse Hierarchical Implicit Neural Representations, *arXiv, 2022*. [[Paper](https://arxiv.org/pdf/2210.02299.pdf)] [[Code](https://github.com/PRBonn/SHINE_mapping)]
- **IRMCL**: Implicit Representation-based Online Global Localization, *arXiv, 2022*. [[Paper](https://arxiv.org/pdf/2210.03113.pdf)] [[Code](https://github.com/PRBonn/ir-mcl)]
- Efficient Implicit Neural Reconstruction Using LiDAR, *ICRA, 2023*. [[Paper](https://arxiv.org/pdf/2302.14363.pdf)] [[Website](http://starydy.xyz/EINRUL/)] [[Pytorch Code](https://github.com/StarRealMan/EINRUL)] [[Video](https://www.youtube.com/watch?v=wUp2I-X-IdI)]
- **NeRF-LOAM**: Neural Implicit Representation for Large-Scale Incremental LiDAR Odometry and Mapping, *ICCV, 2023*. [[Paper](https://arxiv.org/pdf/2303.10709.pdf)] [[Code](https://github.com/JunyuanDeng/NeRF-LOAM)]
- **NF-Atlas**: Multi-Volume Neural Feature Fields for Large Scale LiDAR Mapping, *arXiv, 2023*. [[Paper](https://arxiv.org/pdf/2304.04624.pdf)]
- Accurate Implicit Neural Mapping with More Compact Representation in Large-scale Scenes Using Ranging Data, *RAL, 2023*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10238795)]
- **LONER**: LiDAR Only Neural Representations for Real-Time SLAM, *RAL, 2023*. [[Paper](https://arxiv.org/pdf/2309.04937.pdf)]
- PIN-SLAM: LiDAR SLAM Using a Point-Based Implicit Neural Representation for Achieving Global Map Consistency, *TRO, 2024*. [[Paper](https://www.ipb.uni-bonn.de/wp-content/papercite-data/pdf/pan2024tro.pdf)] [[Code](https://github.com/PRBonn/PIN_SLAM)]
- Towards Large-Scale Incremental Dense Mapping using Robot-centric Implicit Neural Representation, *ICRA, 2024*.  [[Paper](https://arxiv.org/pdf/2306.10472.pdf)] [[Code](https://github.com/HITSZ-NRSL/RIM)] [[Video](https://www.youtube.com/watch?v=sHJ4lju6hsk)]
- **TNDF-Fusion**: Implicit Truncated Neural Distance Field for LiDAR Dense Mapping and Localization in Large Urban Environments, *RAL, 2024*.  [[Paper](https://ieeexplore.ieee.org/abstract/document/10598317)]

### Multimodal NeRF SLAM

- Multi-Modal Neural Radiance Field for Monocular Dense SLAM with a Light-Weight ToF Sensor, *ICCV, 2023*. [[Paper](https://arxiv.org/pdf/2308.14383.pdf)]
- NeuRSS: Enhancing AUV Localization and Bathymetric Mapping with Neural Rendering for Sidescan SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.05807)]


### 3D Gaussian Splatting Visual-SLAM

* **GS-SLAM**: Dense Visual SLAM with 3D Gaussian Splatting, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2311.11700.pdf)]
* **Photo-SLAM**: Real-time Simultaneous Localization and Photorealistic Mapping for Monocular, Stereo, and RGB-D Cameras, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2311.16728.pdf)]
* **SplaTAM**: Splat, Track & Map 3D Gaussians for Dense RGB-D SLAM, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2312.02126.pdf)] [[Website](https://spla-tam.github.io/)] [[Code](https://github.com/spla-tam/SplaTAM)]
* Gaussian Splatting SLAM, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2312.06741.pdf)] [[Code](https://github.com/muskie82/MonoGS)] [[Website](https://rmurai.co.uk/projects/GaussianSplattingSLAM/)]
* **Gaussian-SLAM**: Photo-realistic Dense SLAM with Gaussian Splatting, *arXiv, 2023*. [[Paper](https://arxiv.org/pdf/2312.10070.pdf)] [[Code](https://github.com/VladimirYugay/Gaussian-SLAM)] [[Website](https://vladimiryugay.github.io/gaussian_slam/)]
* **SGS-SLAM**: Semantic Gaussian Splatting For Neural Dense SLAM,  *ECCV, 2024*. [[Paper](https://arxiv.org/pdf/2402.03246.pdf)]
* SemGauss-SLAM: Dense Semantic Gaussian Splatting SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.07494.pdf)]
* Compact 3D Gaussian Splatting For Dense Visual SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.11247.pdf)]
* **NEDS-SLAM**: A Novel Neural Explicit Dense Semantic SLAM Framework using 3D Gaussian Splatting, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.11679.pdf)]
* High-Fidelity SLAM Using Gaussian Splatting with Rendering-Guided Densification and Regularized Optimization, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.12535.pdf)]
* RGBD GS-ICP SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.12550.pdf)] [[Code](https://github.com/Lab-of-AI-and-Robotics/GS_ICP_SLAM)]
* **EndoGSLAM**: Real-Time Dense Reconstruction and Tracking in Endoscopic Surgeries using Gaussian Splatting, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.15124.pdf)] [[Website](https://endogslam.loping151.com/)]
* **CG-SLAM**: Efficient Dense RGB-D SLAM in a Consistent Uncertainty-aware 3D Gaussian Field, *arXiv, 2023*. [[Paper](https://arxiv.org/pdf/2403.16095.pdf)] [[Code](https://github.com/hjr37/CG-SLAM)] [[Website](https://zju3dv.github.io/cg-slam/)]
* **RTG-SLAM**: Real-time 3D Reconstruction at Scale using Gaussian Splatting, *SIGGRAPH, 2024*. [[Paper](https://arxiv.org/pdf/2404.19706)] [[Code](https://github.com/MisEty/RTG-SLAM)]
* **NGM-SLAM**: Gaussian Splatting SLAM with Radiance Field Submap, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.05702)]
* **MotionGS** : Compact Gaussian Splatting SLAM by Motion Filter, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.11129)] [[Code](https://github.com/Antonio521/MotionGS)]
* Monocular Gaussian SLAM with Language Extended Loop Closure, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.13748)]
* **Splat-SLAM**: Globally Optimized RGB-only SLAM with 3D Gaussians, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.16544)] [[Code](https://github.com/eriksandstroem/Splat-SLAM)]
* **MG-SLAM**: Structure Gaussian SLAM with Manhattan World Hypothesis, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.20031)]
* **TAMBRIDGE**: Bridging Frame-Centered Tracking and 3D Gaussian Splatting for Enhanced SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.19614)] [[Code](https://github.com/ZeldaFromHeaven/TAMBRIDGE-DAVID)] [[Website](https://zeldafromheaven.github.io/TAMBRIDGE/)]


### 3D Gaussian Splatting Lidar-SLAM

### Multimodal 3D Gaussian Splatting SLAM
- **LIV-GaussMap**: LiDAR-Inertial-Visual Fusion for Real-time 3D Radiance Field Map Rendering, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2401.14857.pdf)] [[Code](https://github.com/sheng00125/LIV-GaussMap)]
- **HGS-Mapping**: Online Dense Mapping Using Hybrid Gaussian Representation in Urban Scenes, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.20159.pdf)]
- **MM3DGS SLAM**: Multi-modal 3D Gaussian Splatting for SLAM Using Vision, Depth, and Inertial Measurements, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2404.00923.pdf)]
- **MM-Gaussian**: 3D Gaussian-based Multi-modal Fusion for Localization and Reconstruction in Unbounded Scenes, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2404.04026.pdf)]
- **Gaussian-LIC**: Photo-realistic LiDAR-Inertial-Camera SLAM with 3D Gaussian Splatting, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2404.06926.pdf)]

---

## Robotics

### Manipulation/RL

* **Ditto**: Building Digital Twins of Articulated Objects from Interaction, *CVPR, 2022*. [[Paper](https://arxiv.org/abs/2202.08227)] [[Pytorch Code](https://github.com/UT-Austin-RPL/Ditto)] [[Website](https://ut-austin-rpl.github.io/Ditto/)]

* **Relational-NDF**:SE(3)-Equivariant Relational Rearrangement with Neural Descriptor Fields, *CoRL 2022*. [[Paper](https://arxiv.org/pdf/2211.09786.pdf)] [[Pytorch Code](https://github.com/anthonysimeonov/relational_ndf)] [[Website](https://anthonysimeonov.github.io/r-ndf/)]

* **Neural Descriptor Fields**:SE(3)-Equivariant Object Representations for Manipulation, *ICRA, 2022*. [[Paper](https://arxiv.org/abs/2112.05124)] [[Pytorch Code](https://github.com/anthonysimeonov/ndf_robot)] [[Website](https://yilundu.github.io/ndf/)]

* **NeRF-RL**: Reinforcement Learning with Neural Radiance Fields, *arXiv, 2022*. [[Paper](https://dannydriess.github.io/papers/22-driess-NeRF-RL-preprint.pdf)]  [[Website](https://dannydriess.github.io/nerf-rl/)]

* **Neural Motion Fields**: Encoding Grasp Trajectories as Implicit Value Functions, *RSS 2022*. [[Paper](https://arxiv.org/pdf/2206.14854.pdf)]  [[Video](https://youtu.be/B-pEhT1pi-Q)]

* **Grasping Field**: Learning Implicit Representations for Human Grasps, *3DV 2020*. [[Paper](https://arxiv.org/pdf/2008.04451.pdf)] [[Pytorch Code](https://github.com/korrawe/grasping_field)] [[Video](https://youtu.be/J8x5i1FCgTQ)]

* **Dex-NeRF**: Using a Neural Radiance Field to Grasp Transparent Objects, *CoRL, 2021*. [[Paper](https://arxiv.org/abs/2110.14217)]  [[Website](https://sites.google.com/view/dex-nerf)]

* **NeRF-Supervision**: Learning Dense Object Descriptors from Neural Radiance Fields, *ICRA, 2022*. [[Paper](https://arxiv.org/abs/2203.01913)] [[Pytorch Code](https://github.com/yenchenlin/nerf-supervision-public)] [[Website](https://yenchenlin.me/nerf-supervision/)]

* **GIGA**: Synergies Between Affordance and Geometry: 6-DoF Grasp Detection via Implicit Representations, *RSS, 2021*. [[Paper](https://arxiv.org/abs/2104.01542)] [[Pytorch Code](https://github.com/UT-Austin-RPL/GIGA)] [[Website](https://sites.google.com/view/rpl-giga2021)]

* **NeuralGrasps**: Learning Implicit Representations for Grasps of Multiple Robotic Hands, *CoRL, 2022*. [[Paper](https://arxiv.org/abs/2207.02959)] [[Website](https://irvlutd.github.io/NeuralGrasps/)]

* **ObjectFolder**: A Dataset of Objects with Implicit Visual, Auditory, and Tactile Representations, *CoRL, 2021*. [[Paper](https://arxiv.org/pdf/2109.07991.pdf)] [[Pytorch Code](https://github.com/rhgao/ObjectFolder)] [[Website](https://ai.stanford.edu/~rhgao/objectfolder/)]

* **ObjectFolder 2.0**: A Multisensory Object Dataset for Sim2Real Transfer, *CVPR, 2022*. [[Paper](https://arxiv.org/pdf/2204.02389.pdf)] [[Pytorch Code](https://github.com/rhgao/ObjectFolder)] [[Website](https://ai.stanford.edu/~rhgao/objectfolder2.0/)]

* **NeRF2Real**: Sim2real Transfer of Vision-guided Bipedal Motion Skills using Neural Radiance Fields, *arXiv, 2022*. [[Paper](https://arxiv.org/pdf/2210.04932.pdf)] [[Website](https://sites.google.com/view/nerf2real/home)]

* **NiFR**: Neural Fields for Robotic Object Manipulation from a Single Image, *arXiv, 2022*. [[Paper](https://arxiv.org/pdf/2210.12126.pdf)]

* **Local Neural Descriptor Fields**: Locally Conditioned Object Representations for Manipulation, *ICRA, 2023*. [[Paper](https://arxiv.org/pdf/2302.03573.pdf)] [[Code](https://github.com/elchun/lndf_robot)] [[Website](https://elchun.github.io/lndf/)]

* **Equivariant Descriptor Fields**: SE(3)-Equivariant Energy-Based Models for End-to-End Visual Robotic Manipulation Learning, *ICLR, 2023*. [[Paper](https://openreview.net/forum?id=dnjZSPGmY5O)] [[Code](https://github.com/tomato1mule/edf)] 

---

### Planning/Navigation

* **NeRFlow**: Neural Radiance Flow for 4D View Synthesis and Video Processing, *ICCV, 2021*. [[Paper](https://arxiv.org/abs/2012.09790)] [[Pytorch Code](https://github.com/yilundu/nerflow)] [[Website](https://yilundu.github.io/nerflow/)] 

* **NeRF-Navigation**: Vision-Only Robot Navigation in a Neural Radiance World, *ICRA, 2022*. [[Paper](https://mikh3x4.github.io/nerf-navigation/assets/NeRF_Navigation.pdf)] [[Pytorch Code](https://github.com/mikh3x4/nerf-navigation)] [[Website](https://mikh3x4.github.io/nerf-navigation/)] 

* Uncertainty Guided Policy for Active Robotic 3D Reconstruction using Neural Radiance Fields, *RAL, 2022*. [[Paper](https://arxiv.org/pdf/2209.08409.pdf)] [[Website](https://www.vis.xyz/pub/robotic-3d-scan-with-nerf/)] 

* **NeRF-dy**: 3D Neural Scene Representations for Visuomotor Control, *CoRL, 2021*. [[Paper](https://arxiv.org/abs/2107.04004)] [[Website](https://3d-representation-learning.github.io/nerf-dy/)] 

* **CompNeRFdyn**: Learning Multi-Object Dynamics with Compositional Neural Radiance Fields, *CoRL, 2022*. [[Paper](https://arxiv.org/pdf/2202.11855.pdf)] [[Website](https://dannydriess.github.io/compnerfdyn/)] 

* **PIFO**: Deep Visual Constraints: Neural Implicit Models for Manipulation Planning from Visual Input, *RAL, 2022*. [[Paper](https://arxiv.org/pdf/2112.04812.pdf)] [[Website](https://sites.google.com/view/deep-visual-constraints)] 

* **RedSDF**: Regularized Deep Signed Distance Fields for Reactive Motion Generation, *IROS, 2022*. [[Paper](https://arxiv.org/abs/2203.04739)] [[Website](https://irosalab.com/2022/02/28/redsdf/)] 

* **ESDF**: Sampling-free obstacle gradients and reactive planning in Neural Radiance Fields, *ICRA, 2022*. [[Paper](https://arxiv.org/abs/2205.01389)]

* Full-Body Visual Self-Modeling of Robot Morphologies, *Science Robotics, 2022*. [[Paper](https://arxiv.org/abs/2205.01389)] [[Pytorch Code](https://github.com/BoyuanChen/visual-selfmodeling)] [[Website](https://robot-morphology.cs.columbia.edu/)]

* **CLIP-Fields**: Open-label semantic navigation with pre-trained VLMs and language models, *arXiv, 2022*. [[Paper](https://arxiv.org/abs/2210.05663)] [[Pytorch Code and Tutorials](https://github.com/notmahi/clip-fields)] [[Website](https://mahis.life/clip-fields/)]

* Renderable Neural Radiance Map for Visual Navigation, *CVPR, 2023*. [[Paper](https://arxiv.org/pdf/2303.00304.pdf)]

* **NeRF-VINS**: A Real-time Neural Radiance Field Map-based Visual-Inertial Navigation System, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2309.09295.pdf)]
* **Splat-Nav**: Safe Real-Time Robot Navigation in Gaussian Splatting Maps, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.02751.pdf)]
* **GaussNav**: Gaussian Splatting for Visual Navigation, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.11625.pdf)]
* Active Implicit Reconstruction Using One-Shot View Planning, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2310.00685)]
* How Many Views Are Needed to Reconstruct an Unknown Object Using NeRF?, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2310.00684)]
* **GS-Planner**: A Gaussian-Splatting-based Planning Framework for Active High-Fidelity Reconstruction, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.10142)]
* NeRF-Enhanced Outpainting for Faithful Field-of-View Extrapolation, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2309.13240)]
* Neural Visibility Field for Uncertainty-Driven Active Mapping, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2406.06948)] [[Website](https://sites.google.com/view/nvf-cvpr24/)]



### Localization

* **Loc-NeRF**: Monte Carlo Localization using Neural Radiance Fields, *ICRA, 2023*. [[Paper](https://arxiv.org/pdf/2209.09050.pdf)]

* **LocNDF**: Neural Distance Field Mapping for Robot Localization, *RAL, 2023*. [[Paper](https://ieeexplore.ieee.org/document/10168941/)] [[Pytorch Code](https://github.com/PRBonn/LocNDF)]

* Leveraging Neural Radiance Fields for Uncertainty-Aware Visual Localization, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2310.06984.pdf)] [[Video](https://drive.google.com/file/d/1YUMlngGFvYY_iPNu9wMA1woxw8432qXh/view?usp=sharing)]
* **The NeRFect Match**: Exploring NeRF Features for Visual Localization, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.09577.pdf)]
* Leveraging Neural Radiance Fields for Uncertainty-Aware Visual Localization, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2310.06984)]
* **NuRF**: Nudging the Particle Filter in Radiance Fields for Robot Visual Localization, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2406.00312)]
* Fast Global Localization on Neural Radiance Field, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2406.12202)]
* Matching Query Image Against Selected NeRF Feature for Efficient and Scalable Localization, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2406.11766)]

### Re-localization

* Camera Relocalization in Shadow-Free Neural Radiance Fields, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2405.14824)]


----

## Citation

If you find this repository useful, please consider citing this list:

```
@misc{doong2022implicitnerfslampaperlist,
    title = {awesome-Implicit-NeRF-SLAM},
    author = {Doong Li},
    journal = {GitHub repository},
    url = {https://github.com/DoongLi/awesome-Implicit-NeRF-SLAM},
    year = {2022},
}
```
