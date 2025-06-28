# UISS-Net: Underwater Image Semantic Segmentation Network

Improving boundary segmentation accuracy in underwater environments using a customized deep learning architecture.

**Overview**

Underwater image segmentation is a crucial task in aquaculture, marine biology, and underwater robotics. The challenging nature of underwater environments—low visibility, turbidity, and color distortion—impacts the performance of existing models like U-Net and PSP-Net. To address this, we propose UISS-Net, a specialized deep learning architecture tailored for underwater semantic segmentation.

**Key Features**

Backbone: ResNet-50 for deep feature extraction

Architecture: U-Net-like encoder-decoder with attention modules

Enhancements:
* Multi-Scale Feature Fusion Network (MSFFN)
* Channel attention mechanism
* Auxiliary feature extraction
Loss Function: Hybrid of Cross-Entropy and Dice Loss
Datasets Used: SUIM and DeepFish
Metrics: Accuracy, Mean IoU (mIoU), Mean Pixel Accuracy (mPA)

**Objectives**
* Enhance semantic segmentation in underwater images
* Improve feature extraction and boundary precision
* Minimize aliasing and class mixing issues
* Benchmark performance using SUIM and DeepFish datasets

**Datasets**
* SUIM (Semantic Underwater Imagery):
1525 labeled images, 8 classes (divers, fish, coral, robots, etc.)
Supports multi-class segmentation

* DeepFish:
40,000 images, with 300 pixel-labeled masks
Focused on binary fish segmentation

**Methodology**

Preprocessing: Resizing, normalization, and augmentation 

Model Architecture: ResNet50 + U-Net with attention modules

Training:
- Loss: Cross-Entropy + Dice Loss
- Optimizer: Adam
- Learning Rate: Cosine scheduler
  
Evaluation: mIoU, Accuracy, and mPA

Visualization: Pixel-wise mask overlays for qualitative analysis

**Results**

DeepFish Dataset

Accuracy: 99.75%

Mean IoU: 92.60%

Mean Pixel Accuracy: 93.92%

SUIM Dataset

Accuracy: 82.02% (Base paper: 86.93%)

Mean IoU: 67.12% (Base paper: 72.09%)

Mean Pixel Accuracy: 80.05% (Base paper: 80.37%)
 
**Resources**
Base Paper DOI: https://doi.org/10.1007/s10499-024-01439-x

SUIM Dataset: https://irvlab.cs.umn.edu/resources/suim-dataset

DeepFish Dataset: https://research.csiro.au/deepfish/
 
