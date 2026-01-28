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

---

## 3. Comparison with State-of-the-Art (GIF Demo)
The following GIFs provide a qualitative comparison between our method and representative state-of-the-art video compression approaches at ultra-low bitrates.
All methods are evaluated under comparable rate constraints, and the examples highlight differences in structural fidelity and temporal consistency.

> **For better visual inspection, we kindly suggest viewing this page at a larger zoom level to more clearly observe the quality differences among compression models.**
> 
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

--- 
## 4. Key Observations and Qualitative Analysis

Based on the visual comparisons above, we highlight several consistent qualitative observations at extremely low bitrates:

- **Structural fidelity.**  
  Our method better preserves global scene layout and object structure, while competing methods often suffer from severe block artifacts or structural collapse when bitrate drops below bpp@0.003.

- **Temporal consistency.**  
  Despite allocating zero bitrate to motion-related latents, our generative reconstruction maintains smoother and more coherent temporal dynamics, whereas other approaches exhibit noticeable flickering, jittering, or frozen regions.

- **Perceptual realism.**  
  Compared to conventional codecs (e.g., VTM, ECM) and learned baselines (e.g., DCVC, GLCVideo), our results demonstrate more natural motion patterns and fewer visually distracting artifacts under comparable rate budgets.


---

## 7. Reproducibility and Code Availability

Due to the double-blind review policy, **training code and model weights are not released at this stage**.  
Upon acceptance, we plan to release:

- Full training and inference code  
- Pre-trained models  
- Scripts for reproducing all visual results shown on this page  

---

## 8. Contact

For questions regarding the visual results or evaluation protocol, please contact the authors after the review process.

