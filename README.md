# PADS-TAL: Padding-Annealed Diffusion Sampling in Text-Aware Latent Space for Robust and Diverse Text-to-Music Generation

This repository contains the source code for the project website of **PADS-TAL**, presented at **ICML 2026**.

🔗 **[Demo Page (Website)](https://pads-tal.github.io/PADS-TAL.io/)**

> [!IMPORTANT]
> **Note on Audio Samples:** The audio samples demonstrated on the project website and stored in this repository were produced by a generative model as demonstration outputs. **Unauthorized reproduction or use is prohibited.**
> 
> **Usage Restriction on `static/audio_samples`:** Any unauthorized copy, reproduction, modification, distribution, or commercial use of the audio assets located in the `static/audio_samples/` directory is strictly prohibited.

---

## 1. Abstract
Text-to-Music diffusion models are increasingly used in real-world applications, yet deployment remains challenging: generations can collapse to limited patterns even with diverse initial noise and prompts, and inference-time diversity control often harms text alignment and fidelity by distorting key prompt cues established in early denoising.

To address this, we propose **Padding-Annealed Diffusion Sampling (PADS)**, which perturbs only a padding-indexed subspace while keeping non-padding conditioning fixed, enabling controlled exploration with reduced semantic drift.

However, in a text-unaware VAE latent space, such exploration is less likely to stay within genre-faithful neighborhoods, limiting genre-consistent diversity. We therefore introduce **Text-Aware Latent (TAL)** space that aligns local neighborhoods with text-implied genre structure, promoting genre-consistent diversity.

Together, the two techniques form a unified pipeline that, compared to prior methods that perturb the full conditioning, achieves a better text alignment–diversity trade-off: at comparable text alignment, it delivers **15.4% higher diversity** with a relatively small fidelity drop, and further improves within-genre diversity by **71.6%**.

---

## 2. Key Methods

### ① PADS (Padding-Annealed Diffusion Sampling)
*   **Mechanism:** Instead of perturbing the entire text conditioning, PADS perturbs only the **padding-indexed subspace** (padding tokens) while keeping the non-padding conditioning fixed.
*   **Effect:** Enables controlled exploration with reduced semantic drift, maintaining key prompt cues while improving generation diversity.

### ② TAL (Text-Aware Latent Space)
*   **Mechanism:** Aligns local neighborhoods in the VAE latent space with the text-implied genre structure.
*   **Effect:** Restricts exploration to genre-faithful neighborhoods, promoting genre-consistent diversity.

---

## 3. Evaluation Models
*   **Baseline:** High audio quality but limited diversity, with occasional genre mismatches.
*   **CADS:** Enhanced diversity, but suffers from semantic drift and degraded audio quality.
*   **PADS (Ours):** Achieves rich diversity while maintaining high audio quality.
*   **PADS-TAL (Ours):** Achieves rich diversity and high audio quality while maintaining strict genre consistency.

---

## 4. Experimental Setup
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
