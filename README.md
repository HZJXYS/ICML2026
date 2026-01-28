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

## 2. Visual Quality of Our Work at Ultra-Low Bitrates

Below we present a direct visual comparison at the **extremely-low bitrate**.

**Sequence:** GIF (1280 x 720), 5 fps, 15 frames  
**Bitrate range:** 0.001 ~ 0.008 (same for all methods)

<p align="center">
  <img src="video/0p001-0p003/1OURS-videoSRC10_1280x720_30-0p0015.gif" width="400">
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="video/0p001-0p003/2OURS-videoSRC01_1280x720_30-0p0015.gif" width="400"><br>
  <em>Sequence A: &nbsp; bpp @ 0.0015 </em>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
 <em>Sequence B: &nbsp; bpp @ 0.0015 </em>
</p>

<p align="center">
  <img src="video/0p003-0p008/2OURs-videoSRC13_1280x720_30-0p0031.gif" width="400">
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="video/0p003-0p008/3OURS-videoSRC12_1280x720_30-0p0062.gif" width="400"><br>
 <em>Sequence C: &nbsp; bpp @ 0.0031 </em>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
 <em>Sequence D: &nbsp; bpp @ 0.0062 </em>
</p>

## 3. Comparison with State-of-the-Art (GIF Demo)
The following GIFs provide a qualitative comparison between our method and representative state-of-the-art video compression approaches at ultra-low bitrates.
All methods are evaluated under comparable rate constraints, and the examples highlight differences in structural fidelity and temporal consistency.

<table align="center">
  <tr>
    <th>Bitrate range</th>
    <th><b>Ground truth</b></th>
    <th><b>Ours</b></th>
    <th>Method A<br>(GLCvideo @ CVPR'23)</th>
    <th>Method A<br>(DCVC)</th>
    <th>Method B<br>(ECM)</th>
    <th>Method B<br>(VTM)</th>
  </tr>

  <!-- ===== Bitrate: 0.001 ~ 0.003 ===== -->
  <tr>
    <td rowspan="2" align="center"><b>0.001 ~ 0.003</b></td>
    <td align="center">
      <img src="video/0p001-0p003/1GT-videoSRC10_1280x720_30.gif" width="300"> 
    </td>
    <td align="center">
      <img src="video/0p001-0p003/1OURS-videoSRC10_1280x720_30-0p0015.gif" width="300"> <br> bpp @ 0.0015
    </td>
    <td align="center">
      <img src="video/0p001-0p003/1GLC-videoSRC10_1280x704_30-0p0078.gif" width="300"><br> bpp @ 0.0078
    </td>
    <td align="center">
      <img src="video/0p001-0p003/1DCVC-videoSRC10_1280x720_30-0p002.gif" width="300"><br> bpp @ 0.002
    </td>
     <td align="center">
      <img src="video/0p001-0p003/1ECM-videoSRC10_1280x720_30_qp50_rec-0p0016.gif" width="300"><br> bpp @ 0.0016
    </td>
    <td align="center">
      <img src="video/0p001-0p003/1VTM-videoSRC10_1280x720_30_qp50_rec-0p0016.gif" width="300"><br> bpp @ 0.0016
    </td>
  </tr>

  <tr> 
    <td align="center">
      <img src="video/0p001-0p003/2GTvideoSRC01_1280x720_30.gif" width="300">
    </td>
    <td align="center">
      <img src="video/0p001-0p003/2OURS-videoSRC01_1280x720_30-0p0015.gif" width="300"><br> bpp @ 0.0015
    </td>
    <td align="center">
      <img src="video/0p001-0p003/2GLC-videoSRC01_1280x704_30-0p0078.gif" width="300"><br> bpp @ 0.0078
    </td>
    <td align="center">
      <img src="video/0p001-0p003/2DCVC-videoSRC01_1280x720_30-0p002.gif" width="300"><br> bpp @ 0.002
    </td>
     <td align="center">
      <img src="video/0p001-0p003/2ECM-videoSRC01_1280x720_30_qp50_rec-0p0016.gif" width="300"><br> bpp @ 0.0016
    </td>
    <td align="center">
      <img src="video/0p001-0p003/2VTM-videoSRC01_1280x720_30_qp50_rec-0p0016.gif" width="300"><br> bpp @ 0.0016
    </td>
  </tr>

  
  <!-- ===== Bitrate: 0.003 ~ 0.008 ===== -->
   <tr>
    <td rowspan="3" align="center"><b>0.003 ~ 0.008</b></td>
    <td align="center">
      <img src="video/0p003-0p008/1GTvideoSRC09_1280x720_25.gif" width="300"> 
    </td>
    <td align="center">
      <img src="video/0p003-0p008/1OURS-videoSRC09_1280x720_25-0p0031.gif" width="300"> <br> bpp @ 0.0031
    </td>
    <td align="center">
      <img src="video/0p003-0p008/1GLC-videoSRC09_1280x704_25-0.0078.gif" width="300"><br> bpp @ 0.0078
    </td>
    <td align="center">
      <img src="video/0p003-0p008/1DCVC-videoSRC09_1280x720_25-0p0047.gif" width="300"><br> bpp @ 0.0047
    </td>
     <td align="center">
      <img src="video/0p003-0p008/1ECM-videoSRC09_1280x720_25_qp45_rec-0p0033.gif" width="300"><br> bpp @ 0.0033
    </td>
    <td align="center">
      <img src="video/0p003-0p008/1VTM-videoSRC09_1280x720_25_qp45_rec-0p0033.gif" width="300"><br> bpp @ 0.0033
    </td>
  </tr>

  <td align="center">
      <img src="video/0p003-0p008/2GT-videoSRC13_1280x720_30.gif" width="300"> 
    </td>
    <td align="center">
      <img src="video/0p003-0p008/2OURs-videoSRC13_1280x720_30-0p0031.gif" width="300"> <br> bpp @ 0.0031
    </td>
    <td align="center">
      <img src="video/0p003-0p008/2GLC-videoSRC13_1280x704_30-0p0078.gif" width="300"><br> bpp @ 0.0078
    </td>
    <td align="center">
      <img src="video/0p003-0p008/2DCVC-videoSRC13_1280x720_30-0p0047.gif" width="300"><br> bpp @ 0.0047
    </td>
     <td align="center">
      <img src="video/0p003-0p008/2ECM-videoSRC13_1280x720_30_qp45_rec-0p0033.gif" width="300"><br> bpp @ 0.0033
    </td>
    <td align="center">
      <img src="video/0p003-0p008/2VTM-videoSRC13_1280x720_30_qp45_rec-0p0033.gif" width="300"><br> bpp @ 0.0033
    </td>
  </tr>

  <td align="center">
      <img src="video/0p003-0p008/3GT-videoSRC12_1280x720_30.gif" width="300"> 
    </td>
    <td align="center">
      <img src="video/0p003-0p008/3OURS-videoSRC12_1280x720_30-0p0062.gif" width="300"> <br> bpp @ 0.0062
    </td>
    <td align="center">
      <img src="video/0p003-0p008/3GLC-videoSRC12_1280x704_30-0p0078.gif" width="300"><br> bpp @ 0.0078
    </td>
    <td align="center">
      <img src="video/0p003-0p008/3DCVC-videoSRC12_1280x720_30-0p010.gif" width="300"><br> bpp @ 0.010
    </td>
     <td align="center">
      <img src="video/0p003-0p008/3ECM-videoSRC12_1280x720_30_qp45_rec0p0033.gif" width="300"><br> bpp @ 0.0033
    </td>
    <td align="center">
      <img src="video/0p003-0p008/3VTM-videoSRC12_1280x720_30_qp45_rec-0p0033.gif" width="300"><br> bpp @ 0.0033
    </td>
  </tr>
</table>




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

