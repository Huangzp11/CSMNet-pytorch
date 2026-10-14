# CSMNet: A Channel–Space Decoupled Network for Spatial Image Steganalysis

Official PyTorch implementation of the paper:

> **CSMNet: A Channel–Space Decoupled Network for Spatial Image Steganalysis**
> Weiping Zou, Zhipeng Huang, Jingyi Dai, and Gengsheng Deng
> Manuscript under review, *IEEE Signal Processing Letters*

---

## Status: code coming soon

**The source code will be released upon publication of the paper.**
This repository currently contains only this README and a `.gitignore` — no code has been uploaded yet.
Star or watch the repository to be notified when the release lands.

---

## Highlights

- **CSMixer** — a channel–space decoupled module that organizes pointwise channel mixing and depthwise local aggregation into **parallel** branches, guided by two measured properties of content-adaptive embedding: cross-channel joint statistics, and the spatial clustering of embedding modifications.
- **CSMNet** — a lightweight steganalysis network built around CSMixer: SRM high-pass preprocessing → CSMixer → a stride-1 depthwise separable convolution block, together with a stationary wavelet transform (SWT) branch; four stride-2 depthwise separable blocks with **high-frequency residual (HFR) protection** during downsampling; global average pooling and a two-stage fully connected head (256→64→2).
- **0.25M parameters and 1.72G FLOPs.**
- Wins **44 of 45** pairwise comparisons across the nine algorithm–embedding-rate settings on BOSSBase+BOWS2, and **+1.33 percentage points** on average over DDE-Net (ahead on all nine settings).
- CSMixer also transfers to four lightweight backbones: Zhu-Net, SiaStegNet, LWENet, and TSNet.

---

## What will be released

- Model definition — SRM preprocessing, CSMixer, HFR-protected downsampling, and the SWT branch
- Training and evaluation scripts (fixed random seed 0, 300 epochs, AdamW, automatic mixed precision)
- SRM filter kernels
- Data-preparation notes — BOSSBase + BOWS2, resized to 256×256 grayscale, with S-UNIWARD / WOW / MiPOD at 0.1/0.2/0.4 bpp
- Scripts to reproduce the main comparison table, the component ablation, and the cross-backbone transfer study

---

## Citation

A BibTeX entry will be added once the paper is published. In the meantime, please cite it as:

```
Weiping Zou, Zhipeng Huang, Jingyi Dai, and Gengsheng Deng,
"CSMNet: A Channel-Space Decoupled Network for Spatial Image Steganalysis,"
under review.
```

---

## Contact

| Author | Email |
| --- | --- |
| Weiping Zou | zwp@ncu.edu.cn |
| Zhipeng Huang | hzp@ncu.edu.cn |
| Jingyi Dai | daijingyi@ncu.edu.cn |
| Gengsheng Deng (corresponding author) | dgsheng@ncu.edu.cn |

School of Mathematics and Computer Sciences, Nanchang University; and Wenzhou Polytechnic University.

---

## License

No license has been granted yet. A license (for example MIT or Apache-2.0) will be added together with the code release.
