## 📖 Introduction

A deep-learning pipeline for object detection on the SkyFusion aerial imagery dataset. We use a Faster R-CNN model to detect objects of interest in high-resolution drone and satellite images.

* **Dataset**: COCO-format aerial images from Roboflow (SkyFusion)  
* **Task**: Object Detection (bounding box prediction)

---

## 🏗️ Architecture

![Architecture Diagram](assets/Faster-R-CNN-Architecture.jpg)

We employ a two-stage detection architecture (Faster R-CNN) with the following components:

1. **Backbone**: ResNet-50 with Feature Pyramid Network (FPN) for multi-scale feature extraction  
2. **Region Proposal Network (RPN)**: Generates candidate object proposals  
3. **ROI Head**: Two parallel heads for classification and bounding-box regression  
4. **Losses**: Combination of classification loss, box regression loss, RPN box loss, and objectness loss

---

## 🛠️ Setup & Installation

**Prerequisites**

```bash
python >=3.8,<3.11
pip install -r requirements.txt
```

**Data**

Download BraTS 2020 dataset from \[[kaggle website](https://www.kaggle.com/datasets/awsaf49/brats20-dataset-training-validation)].

---

## 📊 Predicted & Real images

<table>
  <tr>
    <td><img src="test_example/example_1.png" width="480"/></td>
    <td><img src="test_example/example_2.png" width="480"/></td>
  </tr>
  <tr>
    <td><img src="test_example/example_3.png" width="480"/></td>
    <td><img src="test_example/example_4.png" width="480"/></td>
  </tr>
  <tr>
    <td><img src="test_example/example_5.png" width="480"/></td>
    <td><img src="test_example/example_6.png" width="480"/></td>
  </tr>
</table>

---

## 📊 Benchmarks & Metrics

<table>
  <tr>
    <td colspan="3" align="center"><img src="assets/benchmark_comparison.png" width="960"/></td>
  </tr>
  <tr>
    <td><img src="assets/specificity_curve.png" width="480"/></td>
    <td><img src="assets/dice_curve.png" width="480"/></td>
  </tr>
  <tr>
    <td><img src="assets/loss_curve.png" width="480"/></td>
    <td><img src="assets/precision_curve.png" width="480"/></td>
  </tr>
  <tr>
    <td><img src="assets/sensitivity_curve.png" width="480"/></td>
    <td><img src="assets/iou_curve.png" width="480"/></td>
  </tr>
</table>

---

## 📝 License
- **Code License**: This repository’s **code** is released under the MIT License.
- **Dataset License**: MRI scans and annotations were downloaded from Kaggle and are subject to Kaggle’s dataset license terms. 

---

## 🤝 Contributing & Contact
Feel free to reach out by opening an issue or pull request. For direct questions, you may also contact:
* **Author**: Matin Gharehdaghi matingd.work@gmail.com
* **Acknowledgements**: Thanks to the MICCAI BraTS organizers and the research community.

Feel free to open issues or PRs for improvements!
