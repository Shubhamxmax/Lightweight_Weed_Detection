# Lightweight Weed Detection using YOLOv8

## Dataset

This project uses the **Cotton Weed 12-Class Dataset**, which contains annotated images of common weed species found in cotton fields. The dataset is designed for object detection tasks and follows the YOLO annotation format.

### Dataset Link

https://www.kaggle.com/datasets/vinayakshanawad/cotton-weed-12-class-dataset

### Dataset Characteristics

* Total Classes: **12**
* Task: **Object Detection**
* Annotation Format: **YOLO Format**
* Data Split:

  * Training Set
  * Validation Set
  * Test Set

### Classes

1. Waterhemp
2. MorningGlory
3. Purslane
4. SpottedSpurge
5. Carpetweed
6. Ragweed
7. Eclipta
8. PricklySida
9. PalmerAmaranth
10. Sicklepod
11. Goosegrass
12. Cutleaf

### Objective

The objective of this project is to develop a lightweight weed detection model capable of accurately detecting and localizing weed species while reducing computational complexity and model size.

---

## Repository Structure

### Detection_1.ipynb – DWC2f-Based Lightweight YOLOv8

This notebook explores parameter reduction by replacing the standard YOLOv8 C2f blocks with a custom DWC2f block based on Depthwise Separable Convolutions.

#### Key Modifications

* Replaced selected C2f blocks with custom DWC2f blocks.
* Implemented Depthwise Convolution and Pointwise Convolution.
* Integrated Focal Loss to improve learning on difficult samples.
* Evaluated the effect of architectural modifications on detection performance.

#### Objective

Reduce model parameters and computational complexity while maintaining effective weed detection performance.

---

### Detection_2.ipynb – Channel Reduction-Based Lightweight YOLOv8

This notebook explores parameter reduction by decreasing the number of channels in selected layers of the YOLOv8 architecture.

#### Key Modifications

* Reduced channels in Layer 8.
* Reduced channels in Layer 21.
* Trained and evaluated the modified architecture.
* Compared performance with the baseline YOLOv8 model.

#### Objective

Develop a more compact YOLOv8 architecture with lower memory consumption and reduced computational cost.

---

## Lightweighting Techniques Explored

### Approach 1: DWC2f Replacement

* Replaced standard C2f blocks with custom DWC2f blocks.
* Utilized Depthwise Separable Convolutions.
* Reduced parameters and computational cost.
* Improved model efficiency for lightweight deployment.

### Approach 2: Channel Reduction

* Reduced the number of channels in selected layers.
* Lowered memory usage and parameter count.
* Reduced GFLOPs and computational complexity.
* Created a more compact model architecture.

Both approaches were evaluated to analyze the trade-off between model efficiency and weed detection performance.
