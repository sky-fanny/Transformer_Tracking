# Transformer Tracking

This repository is a paper digest of [Transformer](https://arxiv.org/abs/1706.03762)-related approaches in visual tracking tasks. Currently, tasks in this repository include **Unified Tracking (UT)**, **Single Object Tracking (SOT)** and **3D Single Object Tracking (3DSOT)**. Note that some trackers involving a [Non-Local](https://arxiv.org/abs/1711.07971) attention mechanism are also collected. Papers are listed in alphabetical order of the first character.

### :link:Jump to:
- ### [[Unified Tracking](https://github.com/Little-Podi/Transformer_Tracking#bookmarkunified-tracking-ut)]
- ### [[Single Object Tracking](https://github.com/Little-Podi/Transformer_Tracking#bookmarksingle-object-tracking-sot)]
- ### [[3D Single Object Tracking](https://github.com/Little-Podi/Transformer_Tracking#bookmark3d-single-object-tracking-3dsot)]

Note: I find it hard to trace all tasks that are related to tracking, including Video Object Segmentation (VOS), Multiple Object Tracking (MOT), Video Instance Segmentation (VIS), Video Object Detection (VOD) and Object Re-Identification (ReID). Hence, I discard all other tracking tasks in a previous update. If you are interested, you can find plenty of collections in [this archived verison](https://github.com/Little-Podi/Transformer_Tracking/tree/4cc6050c07dfd4ecbc9f6aa584601a457ed84eb3). Besides, the most recent trend shows that different tracking tasks are coming to the same avenue.



## :star2:Recommendation

### State-of-the-Art Transformer Tracker:two_hearts::two_hearts::two_hearts:

- **GRM** (Generalized Relation Modeling for Transformer Tracking) [[paper](https://arxiv.org/abs/2303.16580)] [[code](https://github.com/Little-Podi/GRM)]
- **AiATrack** (AiATrack: Attention in Attention for Transformer Visual Tracking) [[paper](https://arxiv.org/abs/2207.09603)] [[code](https://github.com/Little-Podi/AiATrack)]

### Helpful Learning Resource for Tracking:thumbsup::thumbsup::thumbsup:

- **(Talk)** Discriminative Appearance-Based Tracking and Segmentation [[video](https://www.youtube.com/watch?v=ILVnBhFq2Ds)], Deep Visual Reasoning with Optimization-Based Network Modules [[video](https://www.youtube.com/watch?v=UR2TlFCrYac)]
- **(Survey)** Visual Object Tracking with Discriminative Filters and Siamese Networks: A Survey and Outlook [[paper](https://arxiv.org/abs/2112.02838)], Transformers in Single Object Tracking: An Experimental Survey [[paper](https://arxiv.org/abs/2302.11867)]
- **(Library)** PyTracking: Visual Tracking Library Based on PyTorch [[code](https://github.com/visionml/pytracking)]
- **(People)** Martin Danelljan@ETH [[web](https://martin-danelljan.github.io/)], Bin Yan@DLUT [[web](https://masterbin-iiau.github.io/)]

### Joint Feature Extraction and Interaction Era:fire::fire::fire:

![](illustration.png)

- #### Advantage

  - Benefit from pre-trained vision Transformer models.
  - Free from randomly initialized correlation modules.
  - More discriminative target-specific feature extraction.
  - Much faster inference and training convergence speed.
  - Simple and generic one-branch tracking framework.

- #### Roadmap

  - 1st step :feet: feature interaction inside the backbone.
    - **SiamAttn** [[CVPR'20](https://github.com/Little-Podi/Transformer_Tracking#cvpr-2020tadatadatada)], **SBT** [[CVPR'22](https://github.com/Little-Podi/Transformer_Tracking#cvpr-2022tadatadatada-1)], **InMo** [[IJCAI'22](https://github.com/Little-Podi/Transformer_Tracking#ijcai-2022)]
  - 2nd step :feet: concatenation-based feature interaction.
    - **STARK** [[ICCV'21](https://github.com/Little-Podi/Transformer_Tracking#iccv-2021tadatadatada)], **SwinTrack** [[NeurIPS'22](https://github.com/Little-Podi/Transformer_Tracking#neurips-2022tadatadatada)]
  - 3rd step :feet: joint feature extraction and interaction.
    - **MixFormer** [[CVPR'22](https://github.com/Little-Podi/Transformer_Tracking#cvpr-2022tadatadatada-1)], **OSTrack** [[ECCV'22](https://github.com/Little-Podi/Transformer_Tracking#eccv-2022tadatadatada-1)], **SimTrack** [[ECCV'22](https://github.com/Little-Podi/Transformer_Tracking#eccv-2022tadatadatada-1)]
  - 4th step :feet: generalized feature interaction and relation modeling.
    - **GRM** [[CVPR'23](https://github.com/Little-Podi/Transformer_Tracking#cvpr-2023tadatadatada-1)]

### Up-to-Date Benchmark Results:rocket::rocket::rocket:

![](performance.png)



## :bookmark:Unified Tracking (UT)

### CVPR 2023:tada::tada::tada:

- **OmniTracker** (OmniTracker: Unifying Object Tracking by Tracking-with-Detection) [[paper](https://arxiv.org/abs/2303.12079)] [~~code~~]
- **UNINEXT** (Universal Instance Perception as Object Discovery and Retrieval) [[paper](https://arxiv.org/abs/2303.06674)] [[code](https://github.com/MasterBin-IIAU/UNINEXT)]

### Preprint 2023

- **SAM-Track** (Segment and Track Anything) [[paper](https://arxiv.org/abs/2305.06558)] [[code](https://github.com/z-x-yang/Segment-and-Track-Anything)]
- **TAM** (Track Anything: Segment Anything Meets Videos) [[paper](https://arxiv.org/abs/2304.11968)] [[code](https://github.com/gaomingqi/Track-Anything)]

### CVPR 2022:tada::tada::tada:

- **UTT** (Unified Transformer Tracker for Object Tracking) [[paper](https://arxiv.org/abs/2203.15175)] [[code](https://github.com/Flowerfan/Trackron)]

### ECCV 2022:tada::tada::tada:

- **Unicorn** (Towards Grand Unification of Object Tracking) [[paper](https://arxiv.org/abs/2207.07078)] [[code](https://github.com/MasterBin-IIAU/Unicorn)]



## :bookmark:Single Object Tracking (SOT)

### CVPR 2023:tada::tada::tada:

- **ARKitTrack** (ARKitTrack: A New Diverse Dataset for Tracking Using Mobile RGB-D Data) [[paper](https://arxiv.org/abs/2303.13885)] [[code](https://github.com/lawrence-cj/ARKitTrack)]
- **ARTrack** (Autoregressive Visual Tracking) [[paper](https://openaccess.thecvf.com/content/CVPR2023/html/Wei_Autoregressive_Visual_Tracking_CVPR_2023_paper.html)] [[code](https://github.com/MIV-XJTU/ARTrack)]
- **DropTrack** (DropMAE: Masked Autoencoders with Spatial-Attention Dropout for Tracking Tasks) [[paper](https://arxiv.org/abs/2304.00571)] [[code](https://github.com/jimmy-dq/DropTrack)]
- **EMT** (Resource-Efficient RGBD Aerial Tracking) [[paper](https://openaccess.thecvf.com/content/CVPR2023/html/Yang_Resource-Efficient_RGBD_Aerial_Tracking_CVPR_2023_paper.html)] [[code](https://github.com/yjybuaa/RGBDAerialTracking)]
- **GRM** (Generalized Relation Modeling for Transformer Tracking) [[paper](https://arxiv.org/abs/2303.16580)] [[code](https://github.com/Little-Podi/GRM)]
- **JointNLT** (Joint Visual Grounding and Tracking with Natural Language Specification) [[paper](https://arxiv.org/abs/2303.12027)] [[code](https://github.com/lizhou-cs/JointNLT)]
- **MAT** (Representation Learning for Visual Object Tracking by Masked Appearance Transfer) [[paper](https://openaccess.thecvf.com/content/CVPR2023/html/Zhao_Representation_Learning_for_Visual_Object_Tracking_by_Masked_Appearance_Transfer_CVPR_2023_paper.html)] [[code](https://github.com/difhnp/MAT)]
- **SeqTrack** (SeqTrack: Sequence to Sequence Learning for Visual Object Tracking) [[paper](https://arxiv.org/abs/2304.14394)] [[code](https://github.com/microsoft/VideoX/tree/master/SeqTrack)]
- **SwinV2** (Revealing the Dark Secrets of Masked Image Modeling) [[paper](https://arxiv.org/abs/2205.13543)] [[code](https://github.com/SwinTransformer/MIM-Depth-Estimation)]
- **TBSI** (Bridging Search Region Interaction with Template for RGB-T Tracking) [[paper](https://openaccess.thecvf.com/content/CVPR2023/html/Hui_Bridging_Search_Region_Interaction_With_Template_for_RGB-T_Tracking_CVPR_2023_paper.html)] [[code](https://github.com/RyanHTR/TBSI)]
- **VideoTrack** (VideoTrack: Learning to Track Objects via Video Transformer) [[paper](https://openaccess.thecvf.com/content/CVPR2023/html/Xie_VideoTrack_Learning_To_Track_Objects_via_Video_Transformer_CVPR_2023_paper.html)] [[code](https://github.com/phiphiphi31/VideoTrack)]
- **ViPT** (Visual Prompt Multi-Modal Tracking) [[paper](https://arxiv.org/abs/2303.10826)] [[code](https://github.com/jiawen-zhu/ViPT)]

### AAAI 2023

- **CTTrack** (Compact Transformer Tracker with Correlative Masked Modeling) [[paper](https://arxiv.org/abs/2301.10938)] [[code](https://github.com/HUSTDML/CTTrack)]
- **GdaTFT** (Global Dilated Attention and Target Focusing Network for Robust Tracking) [[paper](https://underline.io/lecture/69278-global-dilated-attention-and-target-focusing-network-for-robust-tracking)] [~~code~~]
- **TATrack** (Target-Aware Tracking with Long-term Context Attention) [[paper](https://arxiv.org/abs/2302.13840)] [[code](https://github.com/hekaijie123/TATrack)]

### WACV 2023

- **E.T.Track** (Efficient Visual Tracking with Exemplar Transformers) [[paper](https://arxiv.org/abs/2112.09686)] [[code](https://github.com/pblatter/ettrack)]

### ICRA 2023

- **ClimRT** (Continuity-Aware Latent Interframe Information Mining for Reliable UAV Tracking) [[paper](https://arxiv.org/abs/2303.04525)] [[code](https://github.com/vision4robotics/ClimRT)]
- **SGDViT** (SGDViT: Saliency-Guided Dynamic vision Transformer for UAV tracking) [[paper](https://arxiv.org/abs/2303.04378)] [[code](https://github.com/vision4robotics/SGDViT)]

### IROS 2023

- **CDT** (Cascaded Denoising Transformer for UAV Nighttime Tracking) [[paper](https://ieeexplore.ieee.org/document/10093049)] [[code](https://github.com/vision4robotics/CDT)]
- **FDNT** (End-to-End Feature Decontaminated Network for UAV Tracking) [[paper](https://ieeexplore.ieee.org/document/9981882)] [[code](https://github.com/vision4robotics/FDNT)]
- **ScaleAwareDA** (Scale-Aware Domain Adaptation for Robust UAV Tracking) [[paper](https://ieeexplore.ieee.org/document/10111056)] [[code](https://github.com/vision4robotics/ScaleAwareDA)]
- **TRTrack** (Boosting UAV Tracking With Voxel-Based Trajectory-Aware Pre-Training) [[paper](https://ieeexplore.ieee.org/document/10015867)] [[code](https://github.com/vision4robotics/TRTrack)]

### ICASSP 2023

- **MSTL** (Multi-Source Templates Learning for Real-Time Aerial Tracking) [[paper](https://ieeexplore.ieee.org/document/10094642)] [[code](https://github.com/vpx-ecnu/MSTL)]

### Preprint 2023

- **MACFT** (RGB-T Tracking Based on Mixed Attention) [[paper](https://arxiv.org/abs/2304.04264)] [~~code~~]
- **MixViT** (MixFormer: End-to-End Tracking with Iterative Mixed Attention) [[paper](https://arxiv.org/abs/2302.02814)] [[code](https://github.com/MCG-NJU/MixFormer)]
- **ProFormer** (RGBT Tracking via Progressive Fusion Transformer with Dynamically Guided Learning) [[paper](https://arxiv.org/abs/2303.14778)] [~~code~~]

### CVPR 2022:tada::tada::tada:

- **CMTR** (Cross-Modal Target Retrieval for Tracking by Natural Language) [[paper](https://openaccess.thecvf.com/content/CVPR2022W/ODRUM/html/Li_Cross-Modal_Target_Retrieval_for_Tracking_by_Natural_Language_CVPRW_2022_paper.html)] [~~code~~]
- **CSWinTT** (Transformer Tracking with Cyclic Shifting Window Attention) [[paper](https://arxiv.org/abs/2205.03806)] [[code](https://github.com/SkyeSong38/CSWinTT)]
- **GTELT** (Global Tracking via Ensemble of Local Trackers) [[paper](https://arxiv.org/abs/2203.16092)] [[code](https://github.com/ZikunZhou/GTELT)]
- **MixFormer** (MixFormer: End-to-End Tracking with Iterative Mixed Attention) [[paper](https://arxiv.org/abs/2203.11082)] [[code](https://github.com/MCG-NJU/MixFormer)]
- **RBO** (Ranking-Based Siamese Visual Tracking) [[paper](https://arxiv.org/abs/2205.11761)] [[code](https://github.com/sansanfree/RBO)]
- **SBT** (Correlation-Aware Deep Tracking) [[paper](https://arxiv.org/abs/2203.01666)] [[code](https://github.com/phiphiphi31/SBT)]
- **STNet** (Spiking Transformers for Event-Based Single Object Tracking) [[paper](https://openaccess.thecvf.com/content/CVPR2022/html/Zhang_Spiking_Transformers_for_Event-Based_Single_Object_Tracking_CVPR_2022_paper.html)] [[code](https://github.com/Jee-King/CVPR2022_STNet)]
- **TCTrack** (TCTrack: Temporal Contexts for Aerial Tracking) [[paper](https://arxiv.org/abs/2203.01885)] [[code](https://github.com/vision4robotics/TCTrack)]
- **ToMP** (Transforming Model Prediction for Tracking) [[paper](https://arxiv.org/abs/2203.11192)] [[code](https://github.com/visionml/pytracking)]
- **UDAT** (Unsupervised Domain Adaptation for Nighttime Aerial Tracking) [[paper](https://arxiv.org/abs/2203.10541)] [[code](https://github.com/vision4robotics/UDAT)]

### NeurIPS 2022:tada::tada::tada:

- **SwinTrack** (SwinTrack: A Simple and Strong Baseline for Transformer Tracking) [[paper&review](https://openreview.net/forum?id=9h3KsOVXhLZ)] [[code](https://github.com/LitingLin/SwinTrack)]

### ECCV 2022:tada::tada::tada:

- **AiATrack** (AiATrack: Attention in Attention for Transformer Visual Tracking) [[paper](https://arxiv.org/abs/2207.09603)] [[code](https://github.com/Little-Podi/AiATrack)]
- **CIA** (Hierarchical Feature Embedding for Visual Tracking) [[paper](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/4400_ECCV_2022_paper.php)] [[code](https://github.com/zxgravity/CIA)]
- **DMTracker** (Learning Dual-Fused Modality-Aware Representations for RGBD Tracking) [[paper](https://arxiv.org/abs/2211.03055)] [[code](https://github.com/CV-Tracking/DMTracker)]
- **HCAT** (Efficient Visual Tracking via Hierarchical Cross-Attention Transformer) [[paper](https://arxiv.org/abs/2203.13537)] [[code](https://github.com/chenxin-dlut/HCAT)]
- **OSTrack** (Joint Feature Learning and Relation Modeling for Tracking: A One-Stream Framework) [[paper](https://arxiv.org/abs/2203.11991)] [[code](https://github.com/botaoye/OSTrack)]
- **SimTrack** (Backbone is All Your Need: A Simplified Architecture for Visual Object Tracking) [[paper](https://arxiv.org/abs/2203.05328)] [[code](https://github.com/LPXTT/SimTrack)]
- **VOT2022** (The Tenth Visual Object Tracking VOT2022 Challenge Results) [[paper](https://prints.vicos.si/publications/416/the-tenth-visual-object-tracking-vot2022-challenge-results)] [[code](https://www.votchallenge.net/vot2022/trackers.html)]

### AAAI 2022

- **APFNet** (Attribute-Based Progressive Fusion Network for RGBT Tracking) [[paper](https://aaai-2022.virtualchair.net/poster_aaai7747)] [[code](https://github.com/yangmengmeng1997/APFNet)]

### IJCAI 2022

- **InMo** (Learning Target-Aware Representation for Visual Tracking via Informative Interactions) [[paper](https://arxiv.org/abs/2201.02526)] [[code](https://github.com/JudasDie/SOTS)]
- **SparseTT** (SparseTT: Visual Tracking with Sparse Transformers) [[paper](https://arxiv.org/abs/2205.03776)] [[code](https://github.com/fzh0917/SparseTT)]

### MICCAI 2022

- **TLT** (Transformer Lesion Tracker) [[paper](https://arxiv.org/abs/2206.06252)] [[code](https://github.com/TangWen920812/TLT)]

### WACV 2022

- **SiamTPN** (Siamese Transformer Pyramid Networks for Real-Time UAV Tracking) [[paper](https://arxiv.org/abs/2110.08822)] [[code](https://github.com/RISC-NYUAD/SiamTPNTracker)]

### ICRA 2022

- **SCT** (Tracker Meets Night: A Transformer Enhancer for UAV Tracking) [[paper](https://ieeexplore.ieee.org/document/9696362)] [[code](https://github.com/vision4robotics/SCT)]

### ACCV 2022

- **TAT** (Temporal-Aware Siamese Tracker: Integrate Temporal Context for 3D Object Tracking) [[paper](https://openaccess.thecvf.com/content/ACCV2022/html/Lan_Temporal-aware_Siamese_Tracker_Integrate_Temporal_Context_for_3D_Object_Tracking_ACCV_2022_paper.html)] [[code](https://github.com/tqsdyy/TAT)]

### IROS 2022

- **HighlightNet** (HighlightNet: Highlighting Low-Light Potential Features for Real-Time UAV Tracking) [[paper](https://arxiv.org/abs/2208.06818)] [[code](https://github.com/vision4robotics/HighlightNet)]
- **LPAT** (Local Perception-Aware Transformer for Aerial Tracking) [[paper](https://arxiv.org/abs/2208.00662)] [[code](https://github.com/vision4robotics/LPAT)]
- **SiamSA** (Siamese Object Tracking for Vision-Based UAM Approaching with Pairwise Scale-Channel Attention) [[paper](https://arxiv.org/abs/2211.14564)] [[code](https://github.com/vision4robotics/SiamSA)]

### Preprint 2022

- **CEUTrack** (Revisiting Color-Event based Tracking: A Unified Network, Dataset, and Metric) [[paper](https://arxiv.org/abs/2211.11010)] [[code](https://github.com/Event-AHU/COESOT)]
- **FDT** (Feature-Distilled Transformer for UAV Tracking) [~~paper~~] [[code](https://github.com/vision4robotics/FDT-tracker)]
- **ProContEXT** (ProContEXT: Exploring Progressive Context Transformer for Tracking) [[paper](https://arxiv.org/abs/2210.15511)] [[code](https://shorturl.at/jnNT2)]
- **RAMAVT** (On Deep Recurrent Reinforcement Learning for Active Visual Tracking of Space Noncooperative Objects) [[paper](https://arxiv.org/abs/2212.14304)] [[code](https://github.com/Dongzhou-1996/RAMAVT)]
- **SFTransT** (Learning Spatial-Frequency Transformer for Visual Object Tracking) [[paper](https://arxiv.org/abs/2208.08829)] [[code](https://github.com/Tchuanm/SFTransT)]
- **SiamLA** (Learning Localization-Aware Target Confidence for Siamese Visual Tracking) [[paper](https://arxiv.org/abs/2204.14093)] [~~code~~]
- **SPT** (RGBD1K: A Large-scale Dataset and Benchmark for RGB-D Object Tracking) [[paper](https://arxiv.org/abs/2208.09787)] [[code](https://github.com/xuefeng-zhu5/RGBD1K)]
- **TaMOs** (Beyond SOT: It's Time to Track Multiple Generic Objects at Once) [[paper](https://arxiv.org/abs/2212.11920)] [~~code~~]

### CVPR 2021:tada::tada::tada:

- **SiamGAT** (Graph Attention Tracking) [[paper](https://arxiv.org/abs/2011.11204)] [[code](https://github.com/ohhhyeahhh/SiamGAT)]
- **STMTrack** (STMTrack: Template-Free Visual Tracking with Space-Time Memory Networks) [[paper](https://arxiv.org/abs/2104.00324)] [[code](https://github.com/fzh0917/STMTrack)]
- **TMT** (Transformer Meets Tracker: Exploiting Temporal Context for Robust Visual Tracking) [[paper](https://arxiv.org/abs/2103.11681)] [[code](https://github.com/594422814/TransformerTrack)]
- **TransT** (Transformer Tracking) [[paper](https://arxiv.org/abs/2103.15436)] [[code](https://github.com/chenxin-dlut/TransT)]

### ICCV 2021:tada::tada::tada:

- **AutoMatch** (Learn to Match: Automatic Matching Network Design for Visual Tracking) [[paper](https://arxiv.org/abs/2108.00803)] [[code](https://github.com/JudasDie/SOTS)]
- **DTT** (High-Performance Discriminative Tracking with Transformers) [[paper](https://openaccess.thecvf.com/content/ICCV2021/html/Yu_High-Performance_Discriminative_Tracking_With_Transformers_ICCV_2021_paper.html)] [[code](https://github.com/tominute/DTT)]
- **DualTFR** (Learning Tracking Representations via Dual-Branch Fully Transformer Networks) [[paper](https://arxiv.org/abs/2112.02571)] [[code](https://github.com/phiphiphi31/DualTFR)]
- **HiFT** (HiFT: Hierarchical Feature Transformer for Aerial Tracking) [[paper](https://arxiv.org/abs/2108.00202)] [[code](https://github.com/vision4robotics/HiFT)]
- **SAMN** (Learning Spatio-Appearance Memory Network for High-Performance Visual Tracking) [[paper](https://arxiv.org/abs/2009.09669)] [[code](https://github.com/phiphiphi31/DMB)]
- **STARK** (Learning Spatio-Temporal Transformer for Visual Tracking) [[paper](https://arxiv.org/abs/2103.17154)] [[code](https://github.com/researchmm/Stark)]
- **TransT-M** (High-Performance Transformer Tracking) [[paper](https://arxiv.org/abs/2203.13533)] [[code](https://github.com/chenxin-dlut/TransT-M)]
- **VOT2021** (The Ninth Visual Object Tracking VOT2021 Challenge Results) [[paper](https://prints.vicos.si/publications/400/the-ninth-visual-object-tracking-vot2021-challenge-results)] [[code](https://www.votchallenge.net/vot2021/trackers.html)]

### BMVC 2021

- **TAPL** (TAPL: Dynamic Part-Based Visual Tracking via Attention-Guided Part Localization) [[paper](https://arxiv.org/abs/2110.13027)] [~~code~~]

### Preprint 2021

- **TREG** (Target Transformed Regression for Accurate Tracking) [[paper](https://arxiv.org/abs/2104.00403)] [[code](https://github.com/MCG-NJU/TREG)]
- **TrTr** (TrTr: Visual Tracking with Transformer) [[paper](https://arxiv.org/abs/2105.03817)] [[code](https://github.com/tongtybj/TrTr)]
- **VisEvent** (VisEvent: Reliable Object Tracking via Collaboration of Frame and Event Flows) [[paper](https://arxiv.org/abs/2108.05015)] [[code](https://github.com/wangxiao5791509/VisEvent_SOT_Benchmark)]

### CVPR 2020:tada::tada::tada:

- **SiamAttn** (Deformable Siamese Attention Networks for Visual Object Tracking) [[paper](https://arxiv.org/abs/2004.06711)] [[code](https://github.com/msight-tech/research-siamattn)]

### ICPR 2020

- **VTT** (VTT: Long-Term Visual Tracking with Transformers) [[paper](https://pure.qub.ac.uk/en/publications/vtt-long-term-visual-tracking-with-transformers)] [~~code~~]



## :bookmark:3D Single Object Tracking (3DSOT)

### CVPR 2023:tada::tada::tada:

- **CorpNet** (Correlation Pyramid Network for 3D Single Object Tracking) [[paper](https://arxiv.org/abs/2305.09195)] [~~code~~]
- **CXTrack** (CXTrack: Improving 3D Point Cloud Tracking with Contextual Information) [[paper](https://arxiv.org/abs/2211.08542)] [[code](https://github.com/slothfulxtx/cxtrack3d)]

### AAAI 2023

- **GLT-T** (GLT-T: Global-Local Transformer Voting for 3D Single Object Tracking in Point Clouds) [[paper](https://arxiv.org/abs/2211.10927)] [[code](https://github.com/haooozi/GLT-T)]

### IJCAI 2023

- **OSP2B** (OSP2B: One-Stage Point-to-Box Network for 3D Siamese Tracking) [[paper](https://arxiv.org/abs/2304.11584)] [~~code~~]

### Preprint 2023

- **GLT-T++** (GLT-T++: Global-Local Transformer for 3D Siamese Tracking with Ranking Loss) [[paper](https://arxiv.org/abs/2304.00242)] [[code](https://github.com/haooozi/GLT-T)]
- **MBPTrack** (MBPTrack: Improving 3D Point Cloud Tracking with Memory Networks and Box Priors) [[paper](https://arxiv.org/abs/2303.05071)] [~~code~~]
- **MMF-Track** (Multi-Modal Multi-Level Fusion for 3D Single Object Tracking) [[paper](https://arxiv.org/abs/2305.06794)] [~~code~~]
- **StreamTrack** (Modeling Continuous Motion for 3D Point Cloud Object Tracking) [[paper](https://arxiv.org/abs/2303.07605)] [~~code~~]

### CVPR 2022:tada::tada::tada:

- **PTTR** (PTTR: Relational 3D Point Cloud Object Tracking with Transformer) [[paper](https://arxiv.org/abs/2112.02857)] [[code](https://github.com/Jasonkks/PTTR)]

### ECCV 2022:tada::tada::tada:

- **CMT** (CMT: Context-Matching-Guided Transformer for 3D Tracking in Point Clouds) [[paper](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/1253_ECCV_2022_paper.php)] [[code](https://github.com/jasongzy/CMT)]
- **SpOT** (SpOT: Spatiotemporal Modeling for 3D Object Tracking) [[paper](https://arxiv.org/abs/2207.05856)] [~~code~~]
- **STNet** (3D Siamese Transformer Network for Single Object Tracking on Point Clouds) [[paper](https://arxiv.org/abs/2207.11995)] [[code](https://github.com/fpthink/STNet)]

### Preprint 2022

- **OST** (OST: Efficient One-stream Network for 3D Single Object Tracking in Point Clouds) [[paper](https://arxiv.org/abs/2210.08518)] [~~code~~]
- **PCET** (Implicit and Efficient Point Cloud Completion for 3D Single Object Tracking) [[paper](https://arxiv.org/abs/2209.00522)] [~~code~~]
- **PTTR++** (Exploring Point-BEV Fusion for 3D Point Cloud Object Tracking with Transformer) [[paper](https://arxiv.org/abs/2208.05216)] [[code](https://github.com/Jasonkks/PTTR)]
- **RDT** (Point Cloud Registration-Driven Robust Feature Matching for 3D Siamese Object Tracking) [[paper](https://arxiv.org/abs/2209.06395)] [~~code~~]

### BMVC 2021

- **LTTR** (3D Object Tracking with Transformer) [[paper](https://arxiv.org/abs/2110.14921)] [[code](https://github.com/3bobo/lttr)]

### IROS 2021

- **PTT** (PTT: Point-Track-Transformer Module for 3D Single Object Tracking in Point Clouds) [[paper](https://arxiv.org/abs/2108.06455)] [[code](https://github.com/shanjiayao/PTT)]