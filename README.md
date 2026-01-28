# Visual Results for Generative Video Compression at Extremely Low Bitrates

This repository provides **visual comparison results** for our ICML submission:

> **Title:***Group-of-Latents: Perceptual Video Compression at Extremely-Low Bitrates via Masked Latent Generative Modeling*  
> **Authors:** *Anonymous submission for ICML review*

The goal of this page is to offer **intuitive visual evidence** of the compression behavior of different methods under **extremely constrained bitrate budgets**, where traditional metrics alone may be insufficient.

---

## 1. Overview

Most conventional video codecs and end-to-end learned codecs attempt to preserve **both spatial structure and temporal motion** by jointly encoding intra- and inter-frame information into the bitstream.  
However, under **extremely low bitrates**, the available rate budget becomes insufficient to faithfully represent both aspects.

Our method prioritizes **structure-preserving representation** by encode only **I-Latent** into bitstream, while utilizing the generative model to efficiently recover the **P-latent** containing video **motion information**. This mechanism enables high-fidelity temporal dynamics reconstruction with zero additional bitrate overhead。

---

## 2. Qualitative Results of our work

Below we present a direct visual comparison at the **extremely-low bitrate**.

**Sequence:** CIF (352×288), 30 fps  
**Bitrate:** XX kbps (same for all methods)

### Ours
<video src="videos/0p001-0p003/1DCVC-videoSRC10_1280x720_30-0p002.gif" controls width="520"></video>

<p align="center">
  <img src="videos/0p001-0p003/1DCVC-videoSRC10_1280x720_30-0p002.gif" width="400">
</p>

### HEVC (x265)
<video src="videos/teaser/hevc.mp4" controls width="520"></video>

### VAE-based Learned Codec
<video src="videos/teaser/vae.mp4" controls width="520"></video>

---

## 3. Visual Comparison Using Animated Frames

To facilitate **quick inspection**, we provide animated visual comparisons.  
All methods are evaluated under **identical bitrate constraints**.

---

### 3.1 2 × 3 Comparison (Recommended for Fast Review)

**Sequence 1 | CIF | XX kbps**

| Ours | HEVC | BPG |
|:----:|:----:|:---:|
| ![](videos/gifs/seq1_ours.gif) | ![](videos/gifs/seq1_hevc.gif) | ![](videos/gifs/seq1_bpg.gif) |

**Observation:**  
Our method better preserves **structural edges and object integrity**, while avoiding severe blocking or texture collapse.

---

### 3.2 3 × N Comparison (Multi-Sequence Evaluation)

The following table shows results across multiple test sequences.

| Sequence | Ours | HEVC | VAE-based |
|:--------:|:----:|:----:|:--------:|
| Seq-01 | ![](videos/gifs/seq1_ours.gif) | ![](videos/gifs/seq1_hevc.gif) | ![](videos/gifs/seq1_vae.gif) |
| Seq-02 | ![](videos/gifs/seq2_ours.gif) | ![](videos/gifs/seq2_hevc.gif) | ![](videos/gifs/seq2_vae.gif) |
| Seq-03 | ![](videos/gifs/seq3_ours.gif) | ![](videos/gifs/seq3_hevc.gif) | ![](videos/gifs/seq3_vae.gif) |

---

### Visual Comparison (Image Denoising / Super-Resolution / etc.)

The following table compares the visual quality of different methods. **Ours** restores more high-frequency details compared to Method A and Method B.

| Input / Low Res | Method A [CVPR'23] | Method B [ICCV'23] | **Ours** | Ground Truth |
| :---: | :---: | :---: | :---: | :---: |
| < img src="assets/results/set1_input.png" width="100%"> | < img src="assets/results/set1_methodA.png" width="100%"> | < img src="assets/results/set1_methodB.png" width="100%"> | < img src="assets/results/set1_ours.png" width="100%"> | < img src="assets/results/set1_gt.png" width="100%"> |
| < img src="assets/results/set2_input.png" width="100%"> | < img src="assets/results/set2_methodA.png" width="100%"> | < img src="assets/results/set2_methodB.png" width="100%"> | < img src="assets/results/set2_ours.png" width="100%"> | < img src="assets/results/set2_gt.png" width="100%"> |

> **Figure 1:** Visual comparison on sample ID 001 and 002. Please zoom in for better view.

---

### Comparison with State-of-the-Art (GIF Demo)

Since static images may not fully reveal temporal consistency, we provide a GIF comparison below showing the transition between the baseline and our method.

| Baseline vs. Ours (Looping) |
| :---: |
| < img src="assets/gifs/comparison_demo.gif" width="600"> |
| *Left: Baseline method results. Right: Our results.* |

---

## 4. Full Video Comparisons (MP4)

For more careful inspection, we also provide full-length video clips.

### Sequence 1
- **Ours**  
<video src="videos/comparisons/seq1/ours.mp4" controls width="420"></video>

- **HEVC**  
<video src="videos/comparisons/seq1/hevc.mp4" controls width="420"></video>

- **VAE-based Codec**  
<video src="videos/comparisons/seq1/vae.mp4" controls width="420"></video>

---

## 5. Notes on Evaluation Protocol

- All methods are evaluated at the **same target bitrate**
- CIF resolution (352×288), YUV 4:2:0, 8-bit
- GOP structure and frame rate are aligned whenever applicable
- No post-processing is applied

---

## 6. Raw CIF Files

For completeness and reproducibility, we also provide raw CIF files:

