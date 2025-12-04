# FireSentry-Benchmark-Dataset
**FireSentry-Benchmark-Dataset** is a multi-modal spatiotemporal benchmark dataset for fine-grained wildfire spread forecasting. This dataset integrates drone observations, environmental parameters, and vegetation characteristics to support advanced wildfire modeling research.

<center> <h2 style="color: #e74c3c; border: 2px solid #e74c3c; padding: 10px; border-radius: 5px; background-color: #fff5f5;"> 🎉 This paper has been accepted to the KDD 26 Dataset and Benchmark Track! 🎉 </h2> </center>

## 📁 Dataset Overview

### 🌍 Regions
- **Region A, B, C, D, E**

### 📸 Drone Observations
- **Modalities**:
  - Infrared video (thermal imaging)
  - Visible light video (RGB imaging)
- **Resolution**: 1280×1024 @ 30fps

### 🔥 Wildfire Masks
- **Annotation Methods**:
  - SAM2 algorithm-generated masks
  - Manual annotations

### 🌦️ Environmental Data
Time-series meteorological parameters:
- Air Quality: PM₂.₅, PM₁₀, CO, SO₂, NO₂, O₃, VOC
- Weather: Temperature, Humidity
- Wind: Speed, Direction

### 🌳 Vegetation Data
Forestry characteristics (spatial distribution maps):
- Land cover type
- Tree species distribution
- Stems per hectare
- Average diameter at breast height
- Canopy density

### 🔐 Data Access
| Data Type | Availability | Access Method |
|-----------|--------------|---------------|
| Region A | Public | ./FireSentry Dataset/Region A |
| Regions B-E | Post-acceptance | Available after paper publication |
| Forestry Data | Restricted | [gscloud.cn](http://www.gscloud.cn/search) |

## 🧪 Benchmark Models Overview

A categorized list of representative wildfire forecasting models, including physical, data-driven, and generative approaches. Each entry contains a brief description and citation.

---
## 📖 Table of Contents

1. [Physical Model](#physical-model)  
2. [Data-Driven Models](#data-driven-models)  
3. [Generative Models](#generative-models)
---

### 🔬 Physical Model
- **WRF-SFIRE**: Weather Research and Forecasting model with the SFIRE module for coupled atmosphere–wildland fire simulation.


### 📈 Data-driven Models
- **Earthformer**: Space–time Transformer architecture tailored for Earth system forecasting.
- **PredRNN**: Recurrent neural network for spatiotemporal predictive learning.

### 🎨 Generative Models
- **MCVD**: Masked Conditional Video Diffusion for prediction, generation, and interpolation.
- **STDiff**: Spatio-temporal diffusion model for continuous stochastic video prediction.
- **VDT**: General-purpose video diffusion transformers via mask modeling.
- **DynamiCrafter**: Animating open-domain images with video diffusion priors.

### 🔥 FiReDiff Paradigm
**Enhanced wildfire-specific versions**: MCVD*, STDiff*, VDT*, DynamiCrafter*.
1. **Video Prediction**  
   • Run the chosen **generative model** on the infrared video modality to predict future frames.  
2. **Fire Mask Segmentation**  
   • Apply **SAM2** to the generated frames to produce accurate fire segmentation masks.  

> 💡 **Note:** The “*” denotes models fine-tuned under the FiReDiff paradigm for optimal wildfire forecasting performance.

### 📊 Evaluation Metrics
We evaluate:
- **Segmentation Quality**: AUPRC, F1-score, IoU, and MSE  
- **Video Generation Quality**: PSNR, SSIM, LPIPS, and FVD


### ❓ Contact
For dataset access requests and technical inquiries:
zhoun24@mails.tsinghua.edu.cn



<details> <summary>Citation</summary>
  
@article{mandel2011coupled,
  title     = {Coupled atmosphere-wildland fire modeling with WRF-Fire version 3.3},
  author    = {Mandel, Jan and Beezley, Jonathan D. and Kochanski, Adam K.},
  journal   = {Geoscientific Model Development Discussions},
  volume    = {4},
  number    = {1},
  pages     = {497--545},
  year      = {2011},
  publisher = {Göttingen, Germany}
}

@article{gao2022earthformer,
  title   = {Earthformer: Exploring space-time transformers for earth system forecasting},
  author  = {Gao, Zhihan and Shi, Xingjian and Wang, Hao and Zhu, Yi and Wang, Yuyang Bernie and Li, Mu and Yeung, Dit-Yan},
  journal = {Advances in Neural Information Processing Systems},
  volume  = {35},
  pages   = {25390--25403},
  year    = {2022}
}

@article{wang2022predrnn,
  title     = {PredRNN: A recurrent neural network for spatiotemporal predictive learning},
  author    = {Wang, Yunbo and Wu, Haixu and Zhang, Jianjin and Gao, Zhifeng and Wang, Jianmin and Yu, Philip S. and Long, Mingsheng},
  journal   = {IEEE Transactions on Pattern Analysis and Machine Intelligence},
  volume    = {45},
  number    = {2},
  pages     = {2208--2225},
  year      = {2022},
  publisher = {IEEE}
}

@article{voleti2022mcvd,
  title   = {MCVD: Masked conditional video diffusion for prediction, generation, and interpolation},
  author  = {Voleti, Vikram and Jolicoeur-Martineau, Alexia and Pal, Chris},
  journal = {Advances in Neural Information Processing Systems},
  volume  = {35},
  pages   = {23371--23385},
  year    = {2022}
}

@inproceedings{ye2024stdiff,
  title     = {STDiff: Spatio-temporal diffusion for continuous stochastic video prediction},
  author    = {Ye, Xi and Bilodeau, Guillaume‑Alexandre},
  booktitle = {Proceedings of the AAAI Conference on Artificial Intelligence},
  volume    = {38},
  number    = {7},
  pages     = {6666--6674},
  year      = {2024}
}

@article{lu2023vdt,
  title   = {VDT: General-purpose video diffusion transformers via mask modeling},
  author  = {Lu, Haoyu and Yang, Guoxing and Fei, Nanyi and Huo, Yuqi and Lu, Zhiwu and Luo, Ping and Ding, Mingyu},
  journal = {arXiv preprint arXiv:2305.13311},
  year    = {2023}
}

@inproceedings{xing2024dynamicrafter,
  title        = {DynamiCrafter: Animating open-domain images with video diffusion priors},
  author       = {Xing, Jinbo and Xia, Menghan and Zhang, Yong and Chen, Haoxin and Yu, Wangbo and Liu, Hanyuan and Liu, Gongye and Wang, Xintao and Shan, Ying and Wong, Tien‑Tsin},
  booktitle    = {European Conference on Computer Vision},
  pages        = {399--417},
  year         = {2024},
  organization = {Springer}
}

@article{ravi2024sam,
  title={Sam 2: Segment anything in images and videos},
  author={Ravi, Nikhila and Gabeur, Valentin and Hu, Yuan-Ting and Hu, Ronghang and Ryali, Chaitanya and Ma, Tengyu and Khedr, Haitham and R{\"a}dle, Roman and Rolland, Chloe and Gustafson, Laura and others},
  journal={arXiv preprint arXiv:2408.00714},
  year={2024}
}

</details> 
