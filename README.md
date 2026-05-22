# PADS-TAL: Padding-Annealed Diffusion Sampling in Text-Aware Latent Space for Robust and Diverse Text-to-Music Generation

This repository contains the source code for the project website of **PADS-TAL**, presented at **ICML 2026**.

🔗 **[Demo Page (Website)](https://pads-tal.github.io/PADS-TAL.io/)**

> [!IMPORTANT]
> **Note on Audio Samples:** The audio samples demonstrated on the project website and stored in this repository were produced by a generative model as demonstration outputs. **Unauthorized reproduction or use is prohibited.**
> 
> **Usage Restriction on `static/audio_samples`:** Any unauthorized copy, reproduction, modification, distribution, or commercial use of the audio assets located in the `static/audio_samples/` directory is strictly prohibited.

---

## 1. Evaluation Models
*   **Baseline:** High audio quality but limited diversity, with occasional genre mismatches.
*   **CADS:** Enhanced diversity, but suffers from semantic drift and degraded audio quality.
*   **PADS (Ours):** Achieves rich diversity while maintaining high audio quality.
*   **PADS-TAL (Ours):** Achieves rich diversity and high audio quality while maintaining strict genre consistency.

---

## 2. Experimental Setup
The demo webpage showcases three main evaluation tasks:

*   **Task 1: Samples with Single Prompts & Fixed Initial Noise**
    *   **Goal:** Evaluates the diversity and fidelity of generated samples given the same initial seed under a specific prompt.
*   **Task 2: Samples with Single Prompts & Random Initial Noise**
    *   **Goal:** Evaluates the diversity of generated samples under random noise initialization.
*   **Task 3: Samples with Various Prompts & Random Initial Noise**
    *   **Goal:** Evaluates within-genre diversity across multiple genre-specific categories (Pop, Electronic, Electronic Pop, and New Age).

---

## Citation
If you find this repository useful, please cite the paper.

```bibtex
@inproceedings{
    yoo2026padstal,
    title={{PADS}-{TAL}: Padding-Annealed Diffusion Sampling in Text-Aware Latent Space for Robust and Diverse Text-to-Music Generation},
    author={Yoo, Taekoan and Jung, Wonkyung and Kim, Kyunghun and Kong, Kyeongbo},
    booktitle={Forty-third International Conference on Machine Learning},
    year={2026},
    url={https://openreview.net/forum?id=c0iisI5tJj}
}
```
