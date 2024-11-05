# awesome-Implicit-NeRF-SLAM [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

This repo contains a curative list of **Implicit Representations and NeRF papers relating to SLAM/Robotics domain**, inspired by [Awesome-Implicit-NeRF-Robotics](https://github.com/zubair-irshad/Awesome-Implicit-NeRF-Robotics) <br>

#### Please feel free to send me [pull requests](https://github.com/DoongLi/awesome-Implicit-NeRF-SLAM/blob/main/how-to-PR.md) or [email](mailto:lidong8421bcd@gmail.com) to add papers! <br>

If you find this repository useful, please consider [citing](#citation) and STARing this list. Feel free to share this list with others!

For an overview of **NeRFs**, checkout the Survey ([Neural Volume Rendering: NeRF And Beyond](https://arxiv.org/abs/2101.05204) and [NeRF: Neural Radiance Field in 3D Vision, A Comprehensive Review](https://arxiv.org/pdf/2210.00379.pdf)), Blog post ([NeRF Explosion 2020](https://dellaert.github.io/NeRF/)) and Collection ([awesome-NeRF](https://github.com/yenchenlin/awesome-NeRF)).

For an overview of 3D Gaussian Splatting papers, checkout the Repository ([awesome-3D-gaussian-splatting](https://github.com/MrNeRF/awesome-3D-gaussian-splatting)).

---

## Overview

  - [NeRF General Model](#nerf-general-model)
  - [Survey Paper](#survey-paper)
  - [Benchmarks](#benchmarks)
  - [Tutorials&Workshops](tutorials-and-workshops)
  - [NeRF SLAM](#nerf-slam)
    - [Visual-SLAM](#Visual-SLAM)
    - [Lidar-SLAM](#Lidar-SLAM)
    - [Multimodal-SLAM](#Multimodal-SLAM)
  - [3DGS SLAM](3dgs-slam)
    - [3D Gaussian Splatting Visual-SLAM](#3d-gaussian-splatting-visual-slam)
    - [3D Gaussian Splatting Lidar-SLAM](#3d-gaussian-splatting-lidar-slam)
    - [Multimodal 3D Gaussian Splatting SLAM](#multimodal-3d-gaussian-splatting-slam)
  - [Robotics](#Robotics)
    - [Manipulation/RL](#manipulationrl)
    - [Planning/Navigation](#planningnavigation)
    - [Localization](#localization)
    - [Re-localization](#re-localization)
  - [Citation](#citation)
  - [Acknowledgement](#acknowledgement)

---

## NeRF General Model

- **NeRF**: Representing Scenes as Neural Radiance Fields for View Synthesis, *ECCV, 2020*. [[Paper](https://arxiv.org/pdf/2003.08934.pdf)] [[Tensorflow Code](https://github.com/bmild/nerf)] [[Webpage](http://tancik.com/nerf)] [[Video](https://www.youtube.com/watch?v=JuH79E8rdKc)] 

* **ShAPO**: Implicit Representations for Multi Object Shape Appearance and Pose Optimization, *ECCV, 2022*. [[Paper](https://arxiv.org/pdf/2207.13691.pdf)] [[Pytorch Code](https://github.com/zubair-irshad/shapo)] [[Webpage](https://zubair-irshad.github.io/projects/ShAPO.html)] [[Video](https://youtu.be/LMg7NDcLDcA)] 
* **NCF**: Neural Correspondence Field for Object Pose Estimation, *ECCV, 2022*. [[Paper](https://arxiv.org/pdf/2208.00113.pdf)] [[Pytorch Code]( https://github.com/LinHuang17/NCF-code)] [[Webpage](https://linhuang17.github.io/NCF/)]
* **Neural-Sim**: Learning to Generate Training Data with NeRF, *ECCV 2022*.  [[Paper](https://arxiv.org/pdf/2207.11368.pdf)] [[Pytorch Code](https://github.com/gyhandy/Neural-Sim-NeRF)] [[Webpage](https://fylwen.github.io/disp6d.html)]
* **SNAKE**: SNAKE: Shape-aware Neural 3D Keypoint Field, *NeurIPS, 2022*. [[Paper](https://arxiv.org/abs/2206.01724.pdf)] [[Pytorch Code](https://github.com/zhongcl-thu/SNAKE)]
* **NeRF-RPN**: A general framework for object detection in NeRFs, *PR, 2022*. [[Paper](https://arxiv.org/abs/2211.11646)] [[Video](https://youtu.be/M8_4Ih1CJjE)] 
* **nerf2nerf**: Pairwise Registration of Neural Radiance Fields, *ICRA, 2023*.  [[Paper](https://arxiv.org/pdf/2211.01600.pdf)] [[Pytorch Code]( https://github.com/nerf2nerf/nerf2nerf)] [[Webpage](https://nerf2nerf.github.io/)] [[Dataset](https://drive.google.com/drive/folders/1jNpwAv1T1ntjIHUMJ1wABePA2Z8_nRRQ)]
* **iNeRF**: Inverting Neural Radiance Fields for Pose Estimation, *IROS, 2021*. [[Paper](https://arxiv.org/pdf/2012.05877.pdf)] [[Pytorch Code](https://github.com/yenchenlin/iNeRF-public)] [[Website](https://yenchenlin.me/inerf/)] [[Dataset](https://github.com/BerkeleyAutomation/dex-nerf-datasets)]
* **Point-NeRF**: Point-based Neural Radiance Fields, *CVPR, 2022*. [[Paper](https://arxiv.org/pdf/2201.08845.pdf)] [[Pytorch Code](https://github.com/Xharlie/pointnerf)] [[Website](https://xharlie.github.io/projects/project_sites/pointnerf/)]
* **Zip-NeRF**: Anti-Aliased Grid-Based Neural Radiance Fields, *ICCV, 2023*. [[Paper](https://arxiv.org/abs/2304.06706)] [[Website](https://jonbarron.info/zipnerf/)] [[Video](https://www.youtube.com/watch?v=xrrhynRzC8k)]
* **Mip-NeRF 360**: Unbounded Anti-Aliased Neural Radiance Fields, *CVPR, 2022*. [[Paper](https://arxiv.org/abs/2111.12077)] [[JAX Code]( https://github.com/google-research/multinerf)] [[Website](https://jonbarron.info/mipnerf360/)] [[Dataset](http://storage.googleapis.com/gresearch/refraw360/360_v2.zip)] [[Video](https://www.youtube.com/watch?v=zBSH-k9GbV4&feature=youtu.be)]
* **F2-NeRF**: Fast Neural Radiance Field Training with Free Camera Trajectories, *CVPR, 2023*. [[Paper](https://arxiv.org/pdf/2303.15951.pdf)] [[Pytorch Code](https://github.com/totoro97/f2-nerf)] [[Website](https://totoro97.github.io/projects/f2-nerf/)] [[Dataset](https://www.dropbox.com/sh/jmfao2c4dp9usji/AAC7Ydj6rrrhy1-VvlAVjyE_a?dl=0)]
* 3D Gaussian Splatting for Real-Time Radiance Field Rendering, *SIGGRAPH, 2023*. [[Paper](https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/3d_gaussian_splatting_low.pdf)] [[Website](https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/)]
* 2D Gaussian Splatting for Geometrically Accurate Radiance Fields, *SIGGRAPH, 2024*. [[Paper](https://arxiv.org/pdf/2403.17888)] [[Website](https://surfsplatting.github.io/)]  [[Code](https://github.com/hbb1/2d-gaussian-splatting)]
* **Mip-splatting**: Alias-free 3d gaussian splatting, *CVPR, 2024*. [[Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Yu_Mip-Splatting_Alias-free_3D_Gaussian_Splatting_CVPR_2024_paper.pdf)] [[Website](https://niujinshuchong.github.io/mip-splatting/)]  [[Code](https://github.com/autonomousvision/mip-splatting)]

## Survey Paper

- How NeRFs and 3D Gaussian Splatting are Reshaping SLAM: a Survey, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2402.13255.pdf)]
- SLAM Meets NeRF: A Survey of Implicit SLAM Methods, *World Electric Vehicle Journal, 2024*. [[Paper](https://www.mdpi.com/2032-6653/15/3/85)]
- Neural Fields in Robotics: A Survey, *arXiv, 2024*.[[Paper](https://arxiv.org/abs/2410.20220)]
- NeRF in Robotics: A Survey, *arXiv, 2024*.[[Paper](https://arxiv.org/pdf/2405.01333)]

## Benchmarks

- Customizable Perturbation Synthesis for Robust SLAM Benchmarking, *arXiv, 2024*.[[Paper](https://arxiv.org/pdf/2402.08125.pdf)]
- Benchmarking Implicit Neural Representation and Geometric Rendering in Real-Time RGB-D SLAM, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2403.19473.pdf)] [[Code](https://github.com/thua919/NeRF-SLAM-Benchmark-CVPR24)] [[Website](https://vlis2022.github.io/nerf-slam-benchmark/)]
- Benchmarking Neural Radiance Fields for Autonomous Robots: An Overview, *arXiv, 2024*.[[Paper](https://arxiv.org/pdf/2405.05526)]
- From Perfect to Noisy World Simulation: Customizable Embodied Multi-modal Perturbations for SLAM Robustness Benchmarking, *arXiv, 2024*.[[Paper](https://arxiv.org/pdf/2406.16850)] [[Code](https://github.com/Xiaohao-Xu/SLAM-under-Perturbation)]
- Evaluating Modern Approaches in 3D Scene Reconstruction: NeRF vs Gaussian-Based Methods, *arXiv, 2024*.[[Paper](https://arxiv.org/pdf/2408.04268)]

## Tutorials and Workshops

#### Workshops

- **RoboNerF**: 1st Workshop on Neural Fields in Robotics, *ICRA, 2024*. [[Website](https://robonerf.github.io/2024/)] [[Video](https://www.youtube.com/watch?v=jyEZtbXs3fg)]

## NeRF SLAM

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
* Neural Implicit Dense Semantic SLAM, *arXiv, 2023*. [[Paper](https://arxiv.org/pdf/2304.14560.pdf)] [[Code](https://github.com/Yasaman-Haghighi/NeuralImplicitDenseSemanticSLAM)]
* **FMapping**: Factorized Efficient Neural Field Mapping for Real-Time Dense RGB SLAM, *arXiv, 2023*. [[Paper](https://arxiv.org/pdf/2306.00579v1.pdf)] [[Website](https://vlis2022.github.io/fmap/)] [[Code](https://github.com/thua919/FMapping)] 
* **UncLe-SLAM**: Uncertainty Learning for Dense Neural SLAM, *ICCVw, 2023*. [[Paper](https://arxiv.org/pdf/2306.11048.pdf)] [[Code](https://github.com/kev-in-ta/UncLe-SLAM)]
* **iMODE**:Real-Time Incremental Monocular Dense Mapping Using Neural Field, *ICRA, 2023*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10161538)]
* **NISB-Map**: Scalable Mapping With Neural Implicit Spatial Block, *RAL, 2023*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10163242)]
* RGB-D Mapping and Tracking in a Plenoxel Radiance Field, *WACV, 2024*. [[Paper](https://arxiv.org/pdf/2307.03404.pdf)]
* Efficient Map Fusion for Multiple Implicit SLAM Agents, *TIV, 2023*. [[Paper](https://ieeexplore.ieee.org/abstract/document/10189088)]
* **MIPS-Fusion**: Multi-Implicit-Submaps for Scalable and Robust Online Neural RGB-D Reconstruction, *TOG, 2023*. [[Paper](https://arxiv.org/pdf/2308.08741.pdf)]
* **GO-SLAM**: Global Optimization for Consistent 3D Instant Reconstruction, *ICCV, 2023*. [[Paper](https://arxiv.org/pdf/2309.02436.pdf)] [[Website](https://youmi-zym.github.io/projects/GO-SLAM/)] [[Code](https://github.com/youmi-zym/GO-SLAM)] 
* End-to-End RGB-D SLAM with Multi-MLPs Dense Neural Implicit Representations, *RAL, 2023*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10238793)]
* **DynaMoN**: Motion-Aware Fast And Robust Camera Localization for Dynamic NeRF, *arXiv, 2023*. [[Paper](https://arxiv.org/pdf/2309.08927.pdf)] [[Code](https://github.com/HannahHaensen/DynaMoN)] [[Website](https://hannahhaensen.github.io/DynaMoN/)]
* **HI-SLAM**: Monocular Real-time Dense Mapping with Hybrid Implicit Fields, *RAL, 2023*. [[Paper](https://arxiv.org/pdf/2310.04787.pdf)]
* **CP-SLAM**: Collaborative Neural Point-based SLAM, *NeurIPS, 2024*. [[Paper](https://openreview.net/pdf?id=dFSeZm6dTC)] [[Code](https://github.com/hjr37/CP-SLAM)]
* Learning Neural Implicit through Volume Rendering with Attentive Depth Fusion Priors,  *NeurIPS, 2023*. [[Paper](https://arxiv.org/pdf/2310.11598.pdf)] [[Code](https://github.com/MachinePerceptionLab/Attentive_DFPrior)] [[Website](https://machineperceptionlab.github.io/Attentive_DF_Prior/)]
* **NGEL-SLAM**: Neural Implicit Representation-based Global Consistent Low-Latency SLAM System, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2311.09525.pdf)] [[Code](https://github.com/YunxuanMao/ngel_slam)] 
* **SNI-SLAM**: Semantic Neural Implicit SLAM, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2311.11016.pdf)] [[Code](https://github.com/IRMVLab/SNI-SLAM)]
* Implicit Event-RGBD Neural SLAM, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2311.11013.pdf)]
* **DNS SLAM**: Dense Neural Semantic-Informed SLAM, *IROS, 2024*. [[Paper](https://arxiv.org/pdf/2312.00204.pdf)] [Code](https://github.com/Li-Kunyi/dns-slam)]
* **PLGSLAM**: Progressive Neural Scene Represenation with Local to Global Bundle Adjustment, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2312.09866.pdf)] [[Code](https://github.com/dtc111111/plgslam)]
* **NeRF-VO**: Real-Time Sparse Visual Odometry with Neural Radiance Fields, *RAL, 2024*. [[Paper](https://arxiv.org/pdf/2312.13471.pdf)]
* Ternary-type Opacity and Hybrid Odometry for RGB-only NeRF-SLAM, *IROS, 2024*. [[Paper](https://arxiv.org/pdf/2312.13332.pdf)]
* **DN-SLAM**: A Visual SLAM with ORB Features and NeRF Mapping in Dynamic Environments, *Sensors, 2023*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10376402)]
* **NID-SLAM**: Neural Implicit Representation-based RGB-D SLAM in dynamic environments, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2401.01189.pdf)]
* **DDN-SLAM**: Real-time Dense Dynamic Neural Implicit SLAM with Joint Semantic Encoding, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2401.01545.pdf)] [[Code](https://github.com/DrLi-Ming/DDN-SLAM)]
* **Hi-Map**: Hierarchical Factorized Radiance Field for High-Fidelity Monocular Dense Mapping, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2401.03203.pdf)] [[Website](https://vlis2022.github.io/fmap/)] [[Code](https://github.com/thua919/FMapping)]
* **NeuV-SLAM**: Fast Neural Multiresolution Voxel Optimization for RGBD Dense SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2402.02020.pdf)] [[Code](https://github.com/DARYL-GWZ/NeuV-SLAM)]
* **Structerf-SLAM**: Neural implicit representation SLAM for structural environments, *Computers & Graphics, 2024*. [[Paper](https://www.sciencedirect.com/science/article/abs/pii/S0097849324000207)]
* **Loopy-SLAM**: Dense Neural SLAM with Loop Closures, *CVPR, 2024*. [[Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Liso_Loopy-SLAM_Dense_Neural_SLAM_with_Loop_Closures_CVPR_2024_paper.pdf)] [[Code](https://github.com/eriksandstroem/Loopy-SLAM)] [[Website](https://notchla.github.io/Loopy-SLAM/)]
* **Q-SLAM**: Quadric Representations for Monocular SLAM, *CoRL, 2024*. [[Paper](https://arxiv.org/pdf/2403.08125.pdf)]
* **DVN-SLAM**: Dynamic Visual Neural SLAM Based on Local-Global Encoding, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.11776.pdf)]
* **H3-Mapping**: Quasi-Heterogeneous Feature Grids for Real-time Dense Mapping Using Hierarchical Hybrid Representation, *RAL, 2024*. [[Paper](https://arxiv.org/pdf/2403.10821.pdf)] [[Code](https://github.com/SYSU-STAR/H3-Mapping)]
* **Vox-Fusion++**: Voxel-based Neural Implicit Dense Tracking and Mapping with Multi-maps, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.12536.pdf)] [[Code](https://github.com/zju3dv/Vox-Fusion_Plus_Plus)]
* **MUTE-SLAM**: Real-Time Neural SLAM with Multiple Tri-Plane Hash Representations, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.17765.pdf)]
* **GlORIE-SLAM**: Globally Optimized RGB-only Implicit Encoding Point Cloud SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.19549.pdf)] [[Code](https://github.com/zhangganlin/GlORIE-SLAM)] [[Website](https://ganlinzhang.xyz/GlORIE-SLAM/)]
* Efficient 3D Instance Mapping and Localization with Neural Fields, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2403.19797.pdf)] [[Website](https://gtangg12.github.io/iML/)]
* **NeSLAM**: Neural Implicit Mapping and Self-Supervised Feature Tracking With Depth Completion and Denoising, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.20034.pdf)] [[Code](https://github.com/dtc111111/NeSLAM)]
* **KN-SLAM**: Keypoints and Neural Implicit Encoding SLAM, *TIM, 2024*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10474286)]
* **SLAIM**: Robust Dense Neural SLAM for Online Tracking and Mapping, *CVPRw, 2024*. [[Paper](https://arxiv.org/pdf/2404.11419.pdf)] [[Code](https://github.com/vincentcartillier/SLAIM/)] [[Website](https://vincentcartillier.github.io/slaim.html)]
* **EC-SLAM**: Real-time Dense Neural RGB-D SLAM System with Effectively Constrained Global Bundle Adjustment, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2404.13346.pdf)] [[Code](https://github.com/Lightingooo/EC-SLAM)]
* **S3-SLAM**: Sparse Tri-plane Encoding for Neural Implicit SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2404.18284)]
* **DF-SLAM**: Neural Feature Rendering Based on Dictionary Factors Representation for High-Fidelity Dense Visual SLAM System, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2404.17876)] [[Code](https://github.com/funcdecl/DF-SLAM)]
* Neural Graph Mapping for Dense SLAM with Efficient Loop Closure, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.03633)] [[Code](https://github.com/KTH-RPL/neural_graph_mapping)] [[Website](https://kth-rpl.github.io/neural_graph_mapping/)]
* **MGS-SLAM**: Monocular Sparse Tracking and Gaussian Mapping with Depth Smooth Regularization, *RAL, 2024*. [[Paper](https://arxiv.org/pdf/2405.06241)] [[Code](https://github.com/Z-Pengcheng/MGS-SLAM)]
* **VPE-SLAM**: Neural Implicit Voxel-Permutohedral Encoding for SLAM, *ICRA, 2024*. [[Paper](todo)] [[Code](https://github.com/NeuCV-IRMI/VPE-SLAM)]
* **ONeK-SLAM**: A Robust Object-Level Dense SLAM Based on Joint Neural Radiance Fields and Keypoints, *ICRA 2024*. [[Paper](todo)]
* **HERO-SLAM**: Hybrid Enhanced Robust Optimization of Neural SLAM, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2407.18813)] [[Code](https://github.com/hero-slam/HERO-SLAM)] [[Website](https://hero-slam.github.io/)]
* **NeB-SLAM**: Neural Blocks-based Salable RGB-D SLAM for Unknown Scenes, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.15151)]
* **ENeRF-SLAM**:A Dense Endoscopic SLAM With Neural Implicit Representation, *TMRB, 2024*. [[Paper](https://ieeexplore.ieee.org/abstract/document/10542414)] [[Code](https://github.com/Mar-lll/ENeRF-SLAM)]
* IBD-SLAM: Learning Image-Based Depth Fusion for Generalizable SLAM, *CVPR, 2024*. [[Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Yin_IBD-SLAM_Learning_Image-Based_Depth_Fusion_for_Generalizable_SLAM_CVPR_2024_paper.pdf)] [[Website](https://visual-ai.github.io/ibd-slam)]
* **RoDyn-SLAM**: Robust Dynamic Dense RGB-D SLAM with Neural Radiance Fields, *RAL, 2024*. [[Paper](https://arxiv.org/pdf/2407.01303)] [[Code](https://github.com/fudan-zvg/Rodyn-SLAM)]
* **MoD-SLAM**: Monocular Dense Mapping for Unbounded 3D Scene Reconstruction,  *RAL, 2024*. [[Paper](https://arxiv.org/pdf/2402.03762.pdf)]
* Evaluating geometric accuracy of NeRF reconstructions compared to SLAM method,  *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2407.11238)]
* **I2-SLAM**: Inverting Imaging Process for Robust Photorealistic Dense SLAM,  *ECCV, 2024*. [[Paper](https://arxiv.org/abs/2407.11347v1)]
* An Artificial-Intelligence-based SLAM Processor with Scene-adaptive Sampling and Hybrid NeRF Model Training Acceleration,  *TCASAI, 2024*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10595406)]
* **TivNe-SLAM**: Dynamic Mapping and Tracking via Time-Varying Neural Radiance Fields,  *IROS, 2024*. [[Paper](https://arxiv.org/pdf/2310.18917v4)]
* **NIS-SLAM**: Neural Implicit Semantic RGB-D SLAM for 3D Consistent Scene Understanding,  *TVCG, 2024*. [[Paper](https://arxiv.org/pdf/2407.20853)] [[Website](https://zju3dv.github.io/nis_slam/)]
* **DDS-SLAM**: Dense Semantic Neural SLAM for Deforming Endoscopic Scenes, *IROS, 2024*. [Paper] [[Code](https://github.com/IRMVLab/DDS-SLAM)]
* **FI-SLAM**: Feature Fusion and Instance Reconstruction for Neural Implicit SLAM,  *IROS, 2024*. [Paper] [Code]
* **LCP-Fusion**: A Neural Implicit SLAM with Enhanced Local Constraints and Computable Prior,  *IROS, 2024*. [Paper] [[Code](https://github.com/laliwang/LCP-Fusion)]
* **NF-SLAM**: Effective, Normalizing Flow-supported Neural Field representations for object-level visual SLAM in automotive applications, *IROS, 2024*. [Paper] [Code]
* **EvenNICER-SLAM**: Event-based Neural Implicit Encoding SLAM,  *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2410.03812)] [[Code](https://github.com/cs-vision/EvenNICER-SLAM)]
* **NVINS**: Robust Visual Inertial Navigation Fused with NeRF-augmented Camera Pose Regressor and Uncertainty Quantification, *IROS, 2024*. [[Paper](https://arxiv.org/pdf/2404.01400)]
* Optimizing NeRF-based SLAM with Trajectory Smoothness Constraints, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2410.08780)]
* **LRSLAM**: Low-rank Representation of Signed Distance Fields in Dense Visual SLAM System, *ECCV, 2024*. [[Paper](https://www.ecva.net/papers/eccv_2024/papers_ECCV/papers/10364.pdf)]
* Bridging the Gap Between Explicit and Implicit Representations: Cross-Data Association for VSLAM, *TITS, 2024*. [[Paper](https://ieeexplore.ieee.org/abstract/document/10738129)]

---

### Lidar-SLAM

- **SHINE-Mapping**: Large-Scale 3D Mapping Using Sparse Hierarchical Implicit Neural Representations, *ICRA, 2022*. [[Paper](https://arxiv.org/pdf/2210.02299.pdf)] [[Code](https://github.com/PRBonn/SHINE_mapping)]
- **IR-MCL**: Implicit Representation-based Online Global Localization, *RAL, 2023*. [[Paper](https://arxiv.org/pdf/2210.03113.pdf)] [[Code](https://github.com/PRBonn/ir-mcl)]
- Efficient Implicit Neural Reconstruction Using LiDAR, *ICRA, 2023*. [[Paper](https://arxiv.org/pdf/2302.14363.pdf)] [[Website](http://starydy.xyz/EINRUL/)] [[Code](https://github.com/StarRealMan/EINRUL)] [[Video](https://www.youtube.com/watch?v=wUp2I-X-IdI)]
- **NeRF-LOAM**: Neural Implicit Representation for Large-Scale Incremental LiDAR Odometry and Mapping, *ICCV, 2023*. [[Paper](https://arxiv.org/pdf/2303.10709.pdf)] [[Code](https://github.com/JunyuanDeng/NeRF-LOAM)]
- **NF-Atlas**: Multi-Volume Neural Feature Fields for Large Scale LiDAR Mapping, *RAL, 2023*. [[Paper](https://arxiv.org/pdf/2304.04624.pdf)] [[Website](https://yuxuan1206.github.io/NFAtlas/)] [[Code](https://github.com/yuxuan1206/NF-Atlas)]
- Accurate Implicit Neural Mapping with More Compact Representation in Large-scale Scenes Using Ranging Data, *RAL, 2023*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10238795)]
- **LONER**: LiDAR Only Neural Representations for Real-Time SLAM, *RAL, 2023*. [[Paper](https://arxiv.org/pdf/2309.04937.pdf)] [[Website](https://umautobots.github.io/loner)] [[Code](https://github.com/umautobots/LONER)]
- PIN-SLAM: LiDAR SLAM Using a Point-Based Implicit Neural Representation for Achieving Global Map Consistency, *TRO, 2024*. [[Paper](https://www.ipb.uni-bonn.de/wp-content/papercite-data/pdf/pan2024tro.pdf)] [[Code](https://github.com/PRBonn/PIN_SLAM)]
- Towards Large-Scale Incremental Dense Mapping using Robot-centric Implicit Neural Representation, *ICRA, 2024*.  [[Paper](https://arxiv.org/pdf/2306.10472.pdf)] [[Code](https://github.com/HITSZ-NRSL/RIM)] [[Video](https://www.youtube.com/watch?v=sHJ4lju6hsk)]
- **TNDF-Fusion**: Implicit Truncated Neural Distance Field for LiDAR Dense Mapping and Localization in Large Urban Environments, *RAL, 2024*.  [[Paper](https://ieeexplore.ieee.org/abstract/document/10598317)]
- Neural Implicit Representation for Highly Dynamic LiDAR Mapping and Odometry, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.17729)]
- Multi-Agent Neural SLAM for Autonomous Robots, *IROSw, 2024*. [[Paper](https://www.iros2024-cartin.com/papers/Multi-Agent_Neural_SLAM_for_Autonomous_Robots.pdf)]
- A Probabilistic Formulation of LiDAR Mapping with Neural Radiance Fields, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2411.01725)] [[Code](https://github.com/mcdermatt/PLINK)]

### Multimodal NeRF SLAM

- Multi-Modal Neural Radiance Field for Monocular Dense SLAM with a Light-Weight ToF Sensor, *ICCV, 2023*. [[Paper](https://arxiv.org/pdf/2308.14383.pdf)] [[Website](https://zju3dv.github.io/tof_slam/)] [[Code](https://github.com/zju3dv/tof_slam)]
- **NeuRSS**: Enhancing AUV Localization and Bathymetric Mapping with Neural Rendering for Sidescan SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.05807)]
- **Rapid-Mapping**: LiDAR-Visual Implicit Neural Representations for Real-Time Dense Mapping, *RAL, 2024*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10631303&casa_token=FCrHV9Ve6e0AAAAA:pA-LGLz-cGRTT1PoD6C6uU6x6Gkg5dM1OPaVN1VCHKxiRTqTfXkl8nQGjlPMH_97ysgeOt7x)] [[Code](https://github.com/zhw-github/Rapid-Mapping)]
- Neural Surface Reconstruction and Rendering for LiDAR-Visual Systems, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.05310)] [[Code](https://github.com/hku-mars/M2Mapping)]

## 3DGS SLAM

### 3D Gaussian Splatting Visual-SLAM

* **GS-SLAM**: Dense Visual SLAM with 3D Gaussian Splatting, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2311.11700.pdf)] [[Code](https://github.com/yanchi-3dv/diff-gaussian-rasterization-for-gsslam)]
* **Photo-SLAM**: Real-time Simultaneous Localization and Photorealistic Mapping for Monocular, Stereo, and RGB-D Cameras, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2311.16728.pdf)] [[Code](https://github.com/HuajianUP/Photo-SLAM)]
* **SplaTAM**: Splat, Track & Map 3D Gaussians for Dense RGB-D SLAM, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2312.02126.pdf)] [[Website](https://spla-tam.github.io/)] [[Code](https://github.com/spla-tam/SplaTAM)]
* Gaussian Splatting SLAM, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2312.06741.pdf)] [[Code](https://github.com/muskie82/MonoGS)] [[Website](https://rmurai.co.uk/projects/GaussianSplattingSLAM/)]
* **Gaussian-SLAM**: Photo-realistic Dense SLAM with Gaussian Splatting, *arXiv, 2023*. [[Paper](https://arxiv.org/pdf/2312.10070.pdf)] [[Code](https://github.com/VladimirYugay/Gaussian-SLAM)] [[Website](https://vladimiryugay.github.io/gaussian_slam/)]
* **SGS-SLAM**: Semantic Gaussian Splatting For Neural Dense SLAM,  *ECCV, 2024*. [[Paper](https://arxiv.org/pdf/2402.03246.pdf)] [[Code](https://github.com/ShuhongLL/SGS-SLAM)]
* SemGauss-SLAM: Dense Semantic Gaussian Splatting SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.07494.pdf)]
* Compact 3D Gaussian Splatting For Dense Visual SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.11247.pdf)] [[Code](https://github.com/dtc111111/Compact_GSSLAM)]
* **NEDS-SLAM**: A Novel Neural Explicit Dense Semantic SLAM Framework using 3D Gaussian Splatting, *RAL, 2024*. [[Paper](https://arxiv.org/pdf/2403.11679.pdf)]
* High-Fidelity SLAM Using Gaussian Splatting with Rendering-Guided Densification and Regularized Optimization, *IROS, 2024*. [[Paper](https://arxiv.org/pdf/2403.12535.pdf)]
* RGBD GS-ICP SLAM, *ECCV, 2024*. [[Paper](https://arxiv.org/pdf/2403.12550.pdf)] [[Code](https://github.com/Lab-of-AI-and-Robotics/GS_ICP_SLAM)] [[Video](https://www.youtube.com/watch?v=e-bHh_uMMxE)]
* **EndoGSLAM**: Real-Time Dense Reconstruction and Tracking in Endoscopic Surgeries using Gaussian Splatting, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.15124.pdf)] [[Website](https://endogslam.loping151.com/)] [[Code](https://github.com/Loping151/EndoGSLAM)]
* **CG-SLAM**: Efficient Dense RGB-D SLAM in a Consistent Uncertainty-aware 3D Gaussian Field, *ECCV, 2024*. [[Paper](https://arxiv.org/pdf/2403.16095.pdf)] [[Code](https://github.com/hjr37/CG-SLAM)] [[Website](https://zju3dv.github.io/cg-slam/)]
* **RTG-SLAM**: Real-time 3D Reconstruction at Scale using Gaussian Splatting, *SIGGRAPH, 2024*. [[Paper](https://arxiv.org/pdf/2404.19706)] [[Code](https://github.com/MisEty/RTG-SLAM)]
* **NGM-SLAM**: Gaussian Splatting SLAM with Radiance Field Submap, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.05702)]
* **MotionGS** : Compact Gaussian Splatting SLAM by Motion Filter, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.11129)] [[Code](https://github.com/Antonio521/MotionGS)]
* Monocular Gaussian SLAM with Language Extended Loop Closure, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.13748)]
* **Splat-SLAM**: Globally Optimized RGB-only SLAM with 3D Gaussians, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.16544)] [[Code](https://github.com/eriksandstroem/Splat-SLAM)] [[Code Google Version](https://github.com/google-research/Splat-SLAM)]
* **MG-SLAM**: Structure Gaussian SLAM with Manhattan World Hypothesis, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.20031)]
* **TAMBRIDGE**: Bridging Frame-Centered Tracking and 3D Gaussian Splatting for Enhanced SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2405.19614)] [[Code](https://github.com/ZeldaFromHeaven/TAMBRIDGE-DAVID)] [[Website](https://zeldafromheaven.github.io/TAMBRIDGE/)]
* **GS3LAM**: Gaussian Semantic Splatting SLAM, *MM, 2024*. [[Paper](https://openreview.net/pdf?id=juMYrkJlV3)] [[Code](https://github.com/lif314/GS3LAM)]
* **IG-SLAM**: Instant Gaussian SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2408.01126)]
* Towards Real-Time Gaussian Splatting: Accelerating 3DGS through Photometric SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2408.03825)]
* Visual SLAM with 3D Gaussian Primitives and Depth Priors Enabling Novel View Synthesis, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2408.05635)]
* **LoopSplat**: Loop Closure by Registering 3D Gaussian Splats, , *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2408.10154)] [[Code](https://loopsplat.github.io/)] [[Website](https://github.com/GradientSpaces/LoopSplat)]
* GSFusion: Online RGB-D Mapping Where Gaussian Splatting Meets TSDF Fusion, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2408.12677)] [[Code](https://github.com/goldoak/GSFusion)] [[Website](https://gs-fusion.github.io/)]
* **OG-Mapping**: Octree-based Structured 3D Gaussians for Online Dense Mapping, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2408.17223)]
* **UDGS-SLAM**: UniDepth Assisted Gaussian Splatting for Monocular SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.00362)]
* **GEVO**: Memory-Efficient Monocular Visual Odometry Using Gaussians, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.09295)] [[Code](https://github.com/mit-lean/gevo)]
* **GLC-SLAM**: Gaussian Splatting SLAM with Efficient Loop Closure, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.10982)]
* **Hi-SLAM**: Scaling-up Semantics in SLAM with a Hierarchically Categorical Gaussian Splatting, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.12518)]
* **MGSO**: Monocular Real-time Photometric SLAM with Efficient 3D Gaussian Splatting, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.13055)]
* **Go-SLAM**: Grounded Object Segmentation and Localization with Gaussian Splatting SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.16944)]
* **CaRtGS**: Computational Alignment for Real-Time Gaussian Splatting SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2410.00486)] [[Code](https://github.com/DapengFeng/cartgs)] [[Website](https://dapengfeng.github.io/cartgs/)]
* Robust Gaussian Splatting SLAM by Leveraging Loop Closure, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.20111)]
* **ES-Gaussian**: Gaussian Splatting Mapping via Error Space-Based Gaussian Completion, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2410.06613)] [[Website](https://chenlu-china.github.io/ES-Gaussian/)] [[Code](https://github.com/ChenLu-china/ESGaussian)]
* **GS-EVT**: Cross-Modal Event Camera Tracking based on Gaussian Splatting, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.19228)]
* **GSORB-SLAM**: Gaussian Splatting SLAM benefits from ORB features and Transmittance information, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2410.11356)]
* **DG-SLAM**: Robust Dynamic Gaussian Splatting SLAM with Hybrid Pose Optimization, *NeurIPS, 2024*. [[Paper-Abstract](https://nips.cc/virtual/2024/poster/93346)]
* **AG-SLAM**: Active Gaussian Splatting SLAM, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2410.17422)]


### 3D Gaussian Splatting Lidar-SLAM

### Multimodal 3D Gaussian Splatting SLAM

- **LIV-GaussMap**: LiDAR-Inertial-Visual Fusion for Real-time 3D Radiance Field Map Rendering, *RAL, 2024*. [[Paper](https://arxiv.org/pdf/2401.14857.pdf)] [[Code](https://github.com/sheng00125/LIV-GaussMap)]
- **HGS-Mapping**: Online Dense Mapping Using Hybrid Gaussian Representation in Urban Scenes, *RAL, 2024*. [[Paper](https://arxiv.org/pdf/2403.20159.pdf)]
- **MM3DGS SLAM**: Multi-modal 3D Gaussian Splatting for SLAM Using Vision, Depth, and Inertial Measurements, *IROS, 2024*. [[Paper](https://arxiv.org/pdf/2404.00923.pdf)] [[Website](https://vita-group.github.io/MM3DGS-SLAM/)] [[Code](https://github.com/VITA-Group/MM3DGS-SLAM)]
- **MM-Gaussian**: 3D Gaussian-based Multi-modal Fusion for Localization and Reconstruction in Unbounded Scenes, *IROS, 2024*. [[Paper](https://arxiv.org/pdf/2404.04026.pdf)]
- **Gaussian-LIC**: Photo-realistic LiDAR-Inertial-Camera SLAM with 3D Gaussian Splatting, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2404.06926.pdf)]
- **LI-GS**: Gaussian Splatting with LiDAR Incorporated for Accurate Large-Scale Reconstruction, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.12899)]
- **GS-LIVM**: Real-Time Photo-Realistic LiDAR-Inertial-Visual Mapping with Gaussian Splatting, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2410.17084)] [[Code](https://github.com/xieyuser/GS-LIVM)]

---

## Robotics

### Manipulation/RL

* **Ditto**: Building Digital Twins of Articulated Objects from Interaction, *CVPR, 2022*. [[Paper](https://arxiv.org/abs/2202.08227)] [[Code](https://github.com/UT-Austin-RPL/Ditto)] [[Website](https://ut-austin-rpl.github.io/Ditto/)]
* **Relational-NDF**:SE(3)-Equivariant Relational Rearrangement with Neural Descriptor Fields, *CoRL 2022*. [[Paper](https://arxiv.org/pdf/2211.09786.pdf)] [[Code](https://github.com/anthonysimeonov/relational_ndf)] [[Website](https://anthonysimeonov.github.io/r-ndf/)]
* **Neural Descriptor Fields**:SE(3)-Equivariant Object Representations for Manipulation, *ICRA, 2022*. [[Paper](https://arxiv.org/abs/2112.05124)] [[Code](https://github.com/anthonysimeonov/ndf_robot)] [[Website](https://yilundu.github.io/ndf/)]
* Reinforcement Learning with Neural Radiance Fields, *NeurIPS, 2022*. [[Paper](https://dannydriess.github.io/papers/22-driess-NeRF-RL.pdf)]  [[Website](https://dannydriess.github.io/nerf-rl/)]
* **Neural Motion Fields**: Encoding Grasp Trajectories as Implicit Value Functions, *RSS 2022*. [[Paper](https://arxiv.org/pdf/2206.14854.pdf)]  [[Video](https://youtu.be/B-pEhT1pi-Q)]
* **Grasping Field**: Learning Implicit Representations for Human Grasps, *3DV 2020*. [[Paper](https://arxiv.org/pdf/2008.04451.pdf)] [[Code](https://github.com/korrawe/grasping_field)] [[Video](https://youtu.be/J8x5i1FCgTQ)]
* **Dex-NeRF**: Using a Neural Radiance Field to Grasp Transparent Objects, *CoRL, 2021*. [[Paper](https://arxiv.org/abs/2110.14217)]  [[Website](https://sites.google.com/view/dex-nerf)]
* **NeRF-Supervision**: Learning Dense Object Descriptors from Neural Radiance Fields, *ICRA, 2022*. [[Paper](https://arxiv.org/abs/2203.01913)] [[Code](https://github.com/yenchenlin/nerf-supervision-public)] [[Website](https://yenchenlin.me/nerf-supervision/)]
* **GIGA**: Synergies Between Affordance and Geometry: 6-DoF Grasp Detection via Implicit Representations, *RSS, 2021*. [[Paper](https://arxiv.org/abs/2104.01542)] [[Code](https://github.com/UT-Austin-RPL/GIGA)] [[Website](https://sites.google.com/view/rpl-giga2021)]
* **NeuralGrasps**: Learning Implicit Representations for Grasps of Multiple Robotic Hands, *CoRL, 2022*. [[Paper](https://arxiv.org/abs/2207.02959)] [[Website](https://irvlutd.github.io/NeuralGrasps/)]
* **ObjectFolder**: A Dataset of Objects with Implicit Visual, Auditory, and Tactile Representations, *CoRL, 2021*. [[Paper](https://arxiv.org/pdf/2109.07991.pdf)] [[Code](https://github.com/rhgao/ObjectFolder)] [[Website](https://ai.stanford.edu/~rhgao/objectfolder/)]
* **ObjectFolder 2.0**: A Multisensory Object Dataset for Sim2Real Transfer, *CVPR, 2022*. [[Paper](https://arxiv.org/pdf/2204.02389.pdf)] [[Code](https://github.com/rhgao/ObjectFolder)] [[Website](https://ai.stanford.edu/~rhgao/objectfolder2.0/)]
* **NeRF2Real**: Sim2real Transfer of Vision-guided Bipedal Motion Skills using Neural Radiance Fields, *ICRA, 2023*. [[Paper](https://arxiv.org/pdf/2210.04932.pdf)] [[Website](https://sites.google.com/view/nerf2real/home)]
* Neural Fields for Robotic Object Manipulation from a Single Image / One-shot neural fields for 3d object understanding *arXiv, 2022*. [[Paper](https://arxiv.org/pdf/2210.12126.pdf)] [[Website](https://nerfgrasp.github.io/)]
* **Local Neural Descriptor Fields**: Locally Conditioned Object Representations for Manipulation, *ICRA, 2023*. [[Paper](https://arxiv.org/pdf/2302.03573.pdf)] [[Code](https://github.com/elchun/lndf_robot)] [[Website](https://elchun.github.io/lndf/)]
* **Equivariant Descriptor Fields**: SE(3)-Equivariant Energy-Based Models for End-to-End Visual Robotic Manipulation Learning, *ICLR, 2023*. [[Paper](https://openreview.net/forum?id=dnjZSPGmY5O)] [[Code](https://github.com/tomato1mule/edf)] 

---

### Planning/Navigation

* **NeRFlow**: Neural Radiance Flow for 4D View Synthesis and Video Processing, *ICCV, 2021*. [[Paper](https://arxiv.org/abs/2012.09790)] [[Code](https://github.com/yilundu/nerflow)] [[Website](https://yilundu.github.io/nerflow/)] 
* **NeRF-Navigation**: Vision-Only Robot Navigation in a Neural Radiance World, *ICRA, 2022*. [[Paper](https://mikh3x4.github.io/nerf-navigation/assets/NeRF_Navigation.pdf)] [[Code](https://github.com/mikh3x4/nerf-navigation)] [[Website](https://mikh3x4.github.io/nerf-navigation/)] 
* Uncertainty Guided Policy for Active Robotic 3D Reconstruction using Neural Radiance Fields, *RAL, 2022*. [[Paper](https://arxiv.org/pdf/2209.08409.pdf)] [[Website](https://www.vis.xyz/pub/robotic-3d-scan-with-nerf/)] 
* **NeRF-dy**: 3D Neural Scene Representations for Visuomotor Control, *CoRL, 2021*. [[Paper](https://arxiv.org/abs/2107.04004)] [[Website](https://3d-representation-learning.github.io/nerf-dy/)] 
* **CompNeRFdyn**: Learning Multi-Object Dynamics with Compositional Neural Radiance Fields, *CoRL, 2022*. [[Paper](https://arxiv.org/pdf/2202.11855.pdf)] [[Website](https://dannydriess.github.io/compnerfdyn/)] 
* **PIFO**: Deep Visual Constraints: Neural Implicit Models for Manipulation Planning from Visual Input, *RAL, 2022*. [[Paper](https://arxiv.org/pdf/2112.04812.pdf)] [[Website](https://sites.google.com/view/deep-visual-constraints)] 
* **RedSDF**: Regularized Deep Signed Distance Fields for Reactive Motion Generation, *IROS, 2022*. [[Paper](https://arxiv.org/abs/2203.04739)] [[Website](https://irosalab.com/2022/02/28/redsdf/)] 
* **ESDF**: Sampling-free obstacle gradients and reactive planning in Neural Radiance Fields, *ICRA, 2022*. [[Paper](https://arxiv.org/abs/2205.01389)]
* Full-Body Visual Self-Modeling of Robot Morphologies, *Science Robotics, 2022*. [[Paper](https://arxiv.org/abs/2205.01389)] [[Code](https://github.com/BoyuanChen/visual-selfmodeling)] [[Website](https://robot-morphology.cs.columbia.edu/)]
* **CLIP-Fields**: Weakly Supervised Semantic Fields for Robotic Memory, *RSS, 2023*. [[Paper](https://arxiv.org/abs/2210.05663)] [[Code and Tutorials](https://github.com/notmahi/clip-fields)] [[Website](https://mahis.life/clip-fields/)]
* Renderable Neural Radiance Map for Visual Navigation, *CVPR, 2023*. [[Paper](https://arxiv.org/pdf/2303.00304.pdf)] [[Website](https://rllab-snu.github.io/projects/RNR-Map/)]
* **NeRF-VINS**: A Real-time Neural Radiance Field Map-based Visual-Inertial Navigation System, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2309.09295.pdf)]
* **Splat-Nav**: Safe Real-Time Robot Navigation in Gaussian Splatting Maps, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.02751.pdf)]
* **GaussNav**: Gaussian Splatting for Visual Navigation, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.11625.pdf)] [[Code](https://github.com/XiaohanLei/GaussNav)] [[Website](https://xiaohanlei.github.io/projects/GaussNav/)]
* Active Implicit Reconstruction Using One-Shot View Planning, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2310.00685)]
* How Many Views Are Needed to Reconstruct an Unknown Object Using NeRF?, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2310.00684)]
* **GS-Planner**: A Gaussian-Splatting-based Planning Framework for Active High-Fidelity Reconstruction, *IROS, 2024*. [[Paper](https://arxiv.org/pdf/2405.10142)] [[Video](https://www.bilibili.com/video/BV1e1421S7Kh/)]
* NeRF-Enhanced Outpainting for Faithful Field-of-View Extrapolation, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2309.13240)]
* Neural Visibility Field for Uncertainty-Driven Active Mapping, *CVPR, 2024*. [[Paper](https://arxiv.org/pdf/2406.06948)] [[Website](https://sites.google.com/view/nvf-cvpr24/)] [[Code](https://github.com/GaTech-RL2/nvf_cvpr24)]
* **BEINGS**: Bayesian Embodied Image-goal Navigation with Gaussian Splatting, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.10216)] [[Website](https://www.mwg.ink/BEINGS-web/)] [[Code](https://github.com/guaMass/BEINGS)]
* **HGS-Planner**: Hierarchical Planning Framework for Active Scene Reconstruction Using 3D Gaussian Splatting, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.17624)]
* **RT-GuIDE**: Real-Time Gaussian splatting for Information-Driven Exploration, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.18122)] [[Website](https://tyuezhan.github.io/RT_GuIDE/)]
* Active Neural Mapping at Scale, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.20276)]
* **ActiveSplat**: High-Fidelity Scene Reconstruction through Active Gaussian Splatting, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2410.21955)] [[Website](https://li-yuetao.github.io/ActiveSplat/)]
* Active Implicit Object Reconstruction using Uncertainty-guided Next-Best-View Optimization, *RAL, 2023*. [[Paper](https://arxiv.org/pdf/2303.16739)] [[Code](https://github.com/HITSZ-NRSL/ActiveImplicitRecon)]
* **FisherRF**: Active View Selection and Mapping with Radiance Fields Using Fisher Information, *ECCV, 2024*. [[Paper](https://link.springer.com/chapter/10.1007/978-3-031-72624-8_24)] [[Code](https://github.com/JiangWenPL/FisherRF)] [[Website](https://jiangwenpl.github.io/FisherRF/)]

### Localization

* **Loc-NeRF**: Monte Carlo Localization using Neural Radiance Fields, *ICRA, 2023*. [[Paper](https://arxiv.org/pdf/2209.09050.pdf)] [[Code](https://github.com/MIT-SPARK/Loc-NeRF)]
* **LocNDF**: Neural Distance Field Mapping for Robot Localization, *RAL, 2023*. [[Paper](https://ieeexplore.ieee.org/document/10168941/)] [[Code](https://github.com/PRBonn/LocNDF)]
* Leveraging Neural Radiance Fields for Uncertainty-Aware Visual Localization, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2310.06984.pdf)] [[Video](https://drive.google.com/file/d/1YUMlngGFvYY_iPNu9wMA1woxw8432qXh/view?usp=sharing)]
* **The NeRFect Match**: Exploring NeRF Features for Visual Localization, *ECCV, 2024*. [[Paper](https://arxiv.org/pdf/2403.09577.pdf)] [[Website](https://nerfmatch.github.io/)] [[Code](https://github.com/nv-dvl/nerfmatch)]
* Leveraging Neural Radiance Fields for Uncertainty-Aware Visual Localization, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2310.06984)]
* **NuRF**: Nudging the Particle Filter in Radiance Fields for Robot Visual Localization, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2406.00312)]
* Fast Global Localization on Neural Radiance Field, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2406.12202)] [[Code](https://github.com/kmk97/Fast-Loc-NeRF)]
* Matching Query Image Against Selected NeRF Feature for Efficient and Scalable Localization, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2406.11766)]
* Visual Localization in 3D Maps: Comparing Point Cloud, Mesh, and NeRF Representations, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2408.11966)]
* **HGSLoc**: 3DGS-based Heuristic Camera Pose Refinement, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.10925)]
* **GSLoc**: Efficient Camera Pose Refinement via 3D Gaussian Splatting, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2408.11085)] [[Website](https://gsloc.active.vision/)]
* **MULAN-WC**: Multi-Robot Localization Uncertainty-aware Active NeRF with Wireless Coordination, *IROS, 2024*. [[Paper](https://arxiv.org/pdf/2403.13348)]
* **VRS-NeRF**: Visual Relocalization with Sparse Neural Radiance Field, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2404.09271)] [[Code](https://github.com/feixue94/vrs-nerf)]
* **NeRF-Loc**: Visual Localization with Conditional Neural Radiance Field, *ICRA, 2023*. [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10161420&casa_token=xvxGsiWymY0AAAAA:K21qxl7O2Uef-4Gfzqsu_TiA_2GE7EY5Q9iJyawRGZ8sWMKfsxTuANCC7pOcAByT45rS-XIk&tag=1)] [[Code](https://github.com/TencentYoutuResearch/NeRF-Loc)]
* **WSCLoc**: Weakly-Supervised Sparse-View Camera Relocalization via Radiance Field, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.15272)]
* **CROSSFIRE**: Camera Relocalization On Self-Supervised Features from an Implicit Representation, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2403.15272)]
* **GSplatLoc**: Grounding Keypoint Descriptors into 3D Gaussian Splatting for Improved Visual Localization, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.16502)] [[Website](https://gsplatloc.github.io/)] [[Code](https://github.com/haksorus/gsplatloc)]
* **GSLoc**: Visual Localization with 3D Gaussian Splatting, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2410.06165)]
* **LoGS**: Visual Localization via Gaussian Splatting with Fewer Training Images, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2410.11505)] [[Code](https://github.com/YuzhouCheng66/LoGS-experiment)]
* **SplatLoc**: 3D Gaussian Splatting-based Visual Localization for Augmented Reality, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.16502)] [[Website](https://zju3dv.github.io/splatloc/)] [[Code](https://github.com/zhaihongjia/SplatLoc)]


### Re-localization

* Camera Relocalization in Shadow-Free Neural Radiance Fields, *ICRA, 2024*. [[Paper](https://arxiv.org/pdf/2405.14824)]
* **3DGS-ReLoc**: 3D Gaussian Splatting for Map Representation and Visual ReLocalization, *ICCV, 2023*. [[Paper](https://openaccess.thecvf.com/content/ICCV2023/papers/Moreau_CROSSFIRE_Camera_Relocalization_On_Self-Supervised_Features_from_an_Implicit_Representation_ICCV_2023_paper.pdf)] 

### Reconstruction

* **Language-Embedded Gaussian Splats (LEGS)**: Incrementally Building Room-Scale Representations with a Mobile Robot, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2409.18108)] [[Website](https://berkeleyautomation.github.io/LEGS/)]

----

## Citation

If you find this repository useful, please consider citing this list:

```
@misc{dong2022implicitnerfslampaperlist,
    title = {awesome-Implicit-NeRF-SLAM},
    author = {Dong Li},
    howpublished = {\url{https://github.com/DoongLi/awesome-Implicit-NeRF-SLAM}},
    year = {2022},
    note = "[Online; accessed 08-December-2022]"
}
```

## Acknowledgement

We would like to express our appreciation for the repository cited in the paper:

- How NeRFs and 3D Gaussian Splatting are Reshaping SLAM: a Survey, *arXiv, 2024*. [[Paper](https://arxiv.org/pdf/2402.13255.pdf)]
