# SAM 2-Driven Self-Training for Mammogram Segmentation: Zero-Shot Mask Generation via Pseudo-Video

**Mauricio Fernandez M.<sup>1</sup>, Yixiong Liang<sup>1*</sup>, Christopher A. Cochran<sup>2</sup>**

*<sup>1</sup>School of Computer Science, Central South University, Changsha 410083, P.R. China* <br>
*<sup>2</sup>School of Automation, Central South University, Changsha 410083, P.R. China* <br>
*<sup>*</sup>Corresponding author: [yxliang@csu.edu.cn](https://scholar.google.com/citations?user=-7M32PIAAAAJ&hl=en)

### Methodology Overview
<p align="center">
  <img src="assets/images/methodSAM2v6.png" alt="Methodology Overview" style="width:100%;">
</p>
<p align="center">
  <em>Overview of the SAM 2-driven self-training methodology for mammogram segmentation.</em>
</p>

<p align="center">
  <a href="assets/pdf/paper.pdf" class="button">Download PDF</a>
</p>

---

## Abstract
Accurate mammogram segmentation is crucial for breast cancer diagnosis. However, existing Deep Learning methods often require large, annotated datasets, which are time-consuming and expensive to obtain. 

We introduce SAM 2-driven self-training, a novel approach that leverages SAM 2 for efficient and accurate mammogram segmentation. By constructing a pseudo-video sequence from static mammograms, we use SAM 2 video inference to generate initial masks, subsequently applying them for parameter-efficient adaptation of SAM, focusing on the mask decoder, and an automatic point prompt generator for enhanced usability. 

Our method significantly reduces the need for manual annotation while maintaining high accuracy. Evaluations on the mini-MIAS and CBIS-DDSM datasets demonstrate significant improvements in accuracy and efficiency compared to established techniques and the original SAM. This robust solution facilitates rapid mammogram segmentation and aids creating annotated datasets with minimal user intervention.

---

## Key Contributions
1.  **Self-Training for Zero-Shot Mammogram Segmentation:** Developed a novel and efficient self-training methodology that leverages the video mode of SAM 2 to generate accurate pseudo-labels for training a SAM decoder, enabling high-quality mammogram segmentation without the need for manual annotations.
2.  **Application of SAM 2 Video Mode for Static Medical Images:** Adapted SAM 2 video mode for static mammogram segmentation using pseudo video sequences, achieving high zero-shot accuracy.
3.  **Automatic and Interpretable Single-Point Prompt Generation:** Introduced an automatic and interpretable prompting methodology for mammograms.

---

## Visual Overview

### Example Preprocessing
<p align="center">
  <img src="assets/images/Example2.png" alt="Example Preprocessing" style="width:80%;">
</p>
<p align="center">
  <em>Example from the mini-MIAS dataset. Left: Original mammogram with unwanted artifacts. Right: Final segmentation mask.</em>
</p>

### Qualitative Results
<p align="center">
  <img src="assets/images/mdb283_png_results.png" alt="Results Example 1" style="width:100%;"> <br>
  <img src="assets/images/mdb263_png_results.png" alt="Results Example 2" style="width:100%;"> <br>
  <img src="assets/images/mdb099_png_results.png" alt="Results Example 3" style="width:100%;">
</p>
<p align="center">
  <em>Comparison of mammogram segmentation results using different methods on images from the mini-MIAS dataset. (a) Original, (b) Ground Truth, (c) Otsu, (d) Manual Threshold, (e) Original SAM Point, (f) Our work.</em>
</p>

---

## Keywords
SAM 2, Mammogram segmentation, Self-training, Largest Connected Element (LCE)

---

## Citation
If you find this work useful in your research, please consider citing:
```bibtex
@article{TBD}

