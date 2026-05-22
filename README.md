# PADS-TAL: Padding-Annealed Diffusion Sampling in Text-Aware Latent Space for Robust and Diverse Text-to-Music Generation

This repository contains the source code for the project website of **PADS-TAL**, presented at **ICML 2026**.

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

## 4. Experimental Setup & Demo Prompts
The demo webpage showcases three main evaluation tasks across different prompts (excluding audio samples):

### Task 1: Samples with Single Prompts & Fixed Initial Noise
*   **Goal:** Evaluates the diversity and fidelity of generated samples given the same initial seed under a specific prompt.
*   **Prompts Used:**
    *   `tropical house, drums, 105 bpm, dance`
    *   `timpani, soundtrack, 125 bpm, soothing, ambient`
    *   `groove, 125 bpm, dance, upbeat, happy, musical instrument`
    *   `piano, 100 bpm, double bass, light, calm`

### Task 2: Samples with Single Prompts & Random Initial Noise
*   **Goal:** Evaluates the diversity of generated samples under random noise initialization.
*   **Prompts Used:**
    *   **Prompt 1:** `lofi, chill, vinyl noise, mellow, soft drums, warm chords, nostalgic`
    *   **Prompt 2:** `tropical house, drums, 105 bpm, animal, dance, piano`
    *   **Prompt 3:** `jazz, piano trio, swing, live recording feel, warm tone, improvisation`
    *   **Prompt 4:** `hopeful, mellow, acoustic`

### Task 3: Samples with Various Prompts & Random Initial Noise
*   **Goal:** Evaluates within-genre diversity across multiple genre-specific prompts.
*   **Prompts by Genre:**
    *   **Pop**
        *   `110 bpm, bass guitar, hip hop, pop, drums`
        *   `pop, electric guitar, bass guitar, synthesizer, 110 bpm, funky, plucked string instrument`
        *   `inspiring, pop, guitar, 110 bpm, musical instrument, acoustic guitar, dance`
    *   **Electronic**
        *   `upbeat, drum machine, electric piano, 125 bpm, dubstep`
        *   `upbeat, drum and bass, bass, musical instrument, aggressive, instrumental, sampler, electronic, cinematic, 125 bpm`
        *   `synthesizers, inspiring, 125 bpm, summer, spray, waterfall, electronic`
    *   **Electronic Pop**
        *   `110 bpm, passionate, boing, emotional, soulful, electronic pop, love`
        *   `saturday night, boing, electronic pop, double bass, 110 bpm, happiness, groovy, birthday, the synthesizer, piano, inside`
        *   `funky, guitar, electronic pop, 110 bpm, positive, musical instrument, groovy, outside, boing, upbeat`
    *   **New Age**
        *   `emotional, new age, piano`
        *   `115 bpm, tranquil, new-age music, moving, piano, strings, melancholic, lullaby, emotional`
        *   `musical instrument, emotional, piano, moving, peaceful, reflective, relaxed, calm, sentimental, electric piano, new age`

---

## 5. Citation & Researchers
*   **Authors:** Taekoan Yoo*, Wonkyung Jung*, Kyunghun Kim*, Kyeongbo Kong (* Equal contribution)
*   **Affiliation:** Computer Vision & Signal Processing (CVSP) Lab, Pusan National University
*   **Venue:** International Conference on Machine Learning (ICML) 2026
