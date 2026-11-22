# Comparative Study of R-CNN, Fast R-CNN and Faster R-CNN

## Overview
This project presents a comparative study of the evolution of region-based convolutional neural network architectures for object detection: R-CNN, Fast R-CNN, and Faster R-CNN. It combines an architectural survey with practical implementation demonstrations and a pretrained Faster R-CNN experiment.

## Objectives
- Understand the evolution of region-based object detection.
- Explore Selective Search region proposal generation.
- Demonstrate CNN-based feature extraction and region classification.
- Study shared feature extraction and RoI pooling.
- Implement object detection using pretrained Faster R-CNN.
- Analyze detection outputs and inference time.

## Architectures Studied

### 1. R-CNN
A region-based detection pipeline using candidate region generation, CNN feature extraction, and classification.

Our demonstration includes:
- Selective Search proposals
- Region filtering
- ResNet50 feature extraction
- Region classification

**Note:** This is a simplified educational implementation and not a faithful reproduction of the original trained R-CNN detector.

### 2. Fast R-CNN
Fast R-CNN improves efficiency by extracting CNN features from the full image once and sharing those features across proposed regions.

Our demonstration includes:
- VGG16 shared feature extraction
- Region-to-feature-map mapping
- Simplified 7×7 region pooling
- Classification and bounding-box output shape demonstration

**Note:** The detector heads are untrained. The implementation demonstrates the architectural workflow rather than producing valid trained object detection results.

### 3. Faster R-CNN
Faster R-CNN introduces a Region Proposal Network (RPN), integrating region proposal generation into the detection framework.

Our experiment uses:
- Faster R-CNN
- ResNet50-FPN backbone
- COCO pretrained weights
- PyTorch and torchvision
- CPU inference

## Experimental Results

| Image | Detections | Inference Time (ms) |
|---|---:|---:|
| Bus | 5 | 163.81 |
| Roses | 0 | 182.23 |
| Dog | 1 | 100.02 |
| Mountain | 0 | 110.79 |
| Zidane | 9 | 118.16 |

**Average inference time:** 135.00 ms/image

**Average detections:** 3/image

These results were obtained during a CPU-based experimental run and should not be considered a standardized benchmark.

## Repository Contents
- Jupyter notebooks for implementation demonstrations
- Region proposal and classification outputs
- Feature extraction files
- Experimental summary CSVs
- Detection visualizations and plots (where available)

## Limitations
- R-CNN and Fast R-CNN implementations are simplified demonstrations.
- Detector training was not performed for these implementations.
- Faster R-CNN was evaluated using pretrained weights.
- No ground-truth dataset was used for quantitative accuracy evaluation.
- mAP, precision, recall, and IoU metrics were not calculated.
- Inference times depend on hardware and runtime conditions.

## Conclusion
The project demonstrates the conceptual progression from region-based feature extraction in R-CNN to shared feature extraction in Fast R-CNN and integrated proposal generation in Faster R-CNN. The practical experiments illustrate the architectures and provide an example of pretrained object detection.

## Course
**Course:** Essentials of Artificial Intelligence  
**Project:** CA3 – Survey and Mini-Project

