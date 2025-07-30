# FireSentry-Benchmark-Dataset
**FireSentry-Benchmark-Dataset** is a multi-modal spatiotemporal benchmark dataset for fine-grained wildfire spread forecasting. This dataset integrates drone observations, environmental parameters, and vegetation characteristics to support advanced wildfire modeling research.

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
  - Manually validated manual annotations
- **Granularity**: Pixel-level fire segmentation

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
| Region A | Public | ./FireSentry Dataset/regionA |
| Regions B-E | Post-acceptance | Available after paper publication |
| Forestry Data | Restricted | [gscloud.cn](http://www.gscloud.cn/search) |

## 🧪 Benchmark Models

### 🔬 Physical Model
- **WRF-SFIRE**: Weather Research and Forecasting with Fire module

### 📈 Data-driven Models
- **Earthformer**: Earth-specific transformer architecture
- **PredRNN**: Predictive Recurrent Neural Networks

### 🎨 Generative Models
- **MCVD**: Masked Conditional Video Diffusion
- **STDiff**: Spatio-Temporal Diffusion model
- **VDT**: Video Diffusion Transformer
- **DynamiCrafter**: Dynamic scene crafting framework

### 🔥 FiReDiff Paradigm
**Enhanced wildfire-specific versions**: MCVD*, STDiff*, VDT*, DynamiCrafter*.


### 📊 Evaluation Metrics
We evaluate:
- **Segmentation Quality**: AUPRC, F1-score, IoU, and MSE  
- **Video Generation Quality**: PSNR, SSIM, LPIPS, and FVD


### ❓ Contact
For dataset access requests and technical inquiries:
zhoun24@mails.tsinghua.edu.cn

