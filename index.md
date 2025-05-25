---
layout: default # Uses the default layout from the jekyll-theme-minimal
---

# {{ site.title }}

**Mauricio Fernandez M.$^{1}$, Yixiong Liang$^{1\ast}$, Christopher A. Cochran$^{2}$**

*$^{1}$School of Computer Science, Central South University, Changsha 410083, P.R. China* <br>
*$^{2}$School of Automation, Central South University, Changsha 410083, P.R. China* <br>
*$^{\ast}$Corresponding author: yxliang@csu.edu.cn*

<p align="center">
  <a href="assets/pdf/paper.pdf" class="button">Download PDF</a>
  <a href="https://github.com/MauricioFernandezM/Self-TrainingSAM" class="button">View Code on GitHub</a>
  <!-- Add arXiv link if available: <a href="ARXIV_LINK_HERE" class="button">View on arXiv</a> -->
</p>

---

## Abstract
Accurate mammogram segmentation is crucial for breast cancer diagnosis. However, existing Deep Learning methods often require large, annotated datasets, which are time-consuming and expensive to obtain. We introduce SAM 2-driven self-training, a novel approach that leverages SAM 2 for efficient and accurate mammogram segmentation. By constructing a pseudo-video sequence from static mammograms, we use SAM 2 video inference to generate initial masks, subsequently applying them for parameter-efficient adaptation of SAM, focusing on the mask decoder, and an automatic point prompt generator for enhanced usability. Our method significantly reduces the need for manual annotation while maintaining high accuracy. Evaluations on the mini-MIAS and CBIS-DDSM datasets demonstrate significant improvements in accuracy and efficiency compared to established techniques and the original SAM. This robust solution facilitates rapid mammogram segmentation and aids creating annotated datasets with minimal user intervention.

---

## Key Contributions
1.  **Self-Training for Zero-Shot Mammogram Segmentation:** Developed a novel and efficient self-training methodology that leverages the video mode of SAM 2 to generate accurate pseudo-labels for training a SAM decoder, enabling high-quality mammogram segmentation without the need for manual annotations.
2.  **Application of SAM 2 Video Mode for Static Medical Images:** Adapted SAM 2 video mode for static mammogram segmentation using pseudo video sequences, achieving high zero-shot accuracy.
3.  **Automatic and Interpretable Single-Point Prompt Generation:** Introduced an automatic and interpretable prompting methodology for mammograms.

---

## Visual Overview

### Example Preprocessing (Figure 1)
<p align="center">
  <img src="assets/images/fig1_example_preprocessing.png" alt="Example Preprocessing" style="width:80%;">
</p>
*Example from the mini-MIAS dataset. Left: Original mammogram with unwanted artifacts. Right: Final segmentation mask.*

### Methodology Overview (Figure 2)
<p align="center">
  <img src="assets/images/fig2_methodology.png" alt="Methodology Overview" style="width:100%;">
</p>
*Overview of the SAM 2-driven self-training methodology for mammogram segmentation.*

### Qualitative Results (Figure 3)
<p align="center">
  <img src="assets/images/fig3_results_example1.png" alt="Results Example 1" style="width:100%;"> <br>
  <img src="assets/images/fig3_results_example2.png" alt="Results Example 2" style="width:100%;"> <br>
  <img src="assets/images/fig3_results_example3.png" alt="Results Example 3" style="width:100%;">
</p>
*Comparison of mammogram segmentation results using different methods on images from the mini-MIAS dataset. (a) Original, (b) Ground Truth, (c) Otsu, (d) Manual Threshold, (e) Original SAM Point, (f) Our work.*

---

## Keywords
SAM 2, Mammogram segmentation, Self-training, Largest Connected Element (LCE)

---

## Citation
If you find this work useful in your research, please consider citing:
```bibtex
@article{fernandez2024sam2,
  title={{SAM 2-Driven Self-Training for Mammogram Segmentation: Zero-Shot Mask Generation via Pseudo-Video}},
  author={Fernandez M., Mauricio and Liang, Yixiong and Cochran, Christopher A.},
  journal={Proceedings of the IEEE International Conference on Image Processing (ICIP)},
  year={2024}
  % Add month, pages, doi if known when published
}

