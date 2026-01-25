---
layout: project_page
permalink: /

title: PADS-TAL Padding-Annealed Diffusion Sampling in Text Aligned Latent Space for Robust and Diverse Samples
authors:
    anonymous
affiliations:
    

---

<!-- Using HTML to center the abstract -->
<div class="columns is-centered has-text-centered">
    <div class="column is-four-fifths">
        <h2>Abstract</h2>
        <div class="content has-text-justified">
Text-to-Music (T2M) diffusion models are increasingly used in real-world applications, yet reliable deployment remains challenging: generations can collapse to limited patterns, even across different random initial noise seeds, while controlling diversity at inference time remains difficult under strict semantic requirements. Training-free sampling methods such as Condition-Annealed Diffusion Sampling, while effective in Text-to-Image, can be brittle in T2M: increasing early-timestep perturbations often degrades text--audio alignment and fidelity, and does not reliably yield genre-faithful variations. We propose two complementary solutions: Padding-Augmented Diffusion Sampling (PADS), which keeps semantic token embeddings unperturbed and injects timestep-dependent noise only into a padding-indexed subspace, annealing it to zero over timesteps to minimize semantic corruption, and Text-Aligned Latent, a text-aware latent space learned via a redesigned VAE so diffusion sampling occurs in neighborhoods aligned with text-implied global semantics, especially genre. Together, our unified pipeline improves diversity in T2M while maintaining prompt alignment and preserving prompt-specified global attributes.
        </div>
    </div>
</div>


<div align="center">
  <img src="static/image/Figure1.png" width="50%">
</div>

## Audio Examples
### Task 1: [Samples with single Prompts & Fixed Initial Noise]

<table>
  <tr>
    <th>Prompt</th>     
    <th>Baseline</th>     
    <th>CADS</th>     
    <th>Ours</th>
  </tr>
  <tr>
    <td><b>tropical house, drums, 105 bpm, animal, dance, piano</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task3/1120.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task3/1120.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task3/1120.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>carol, 100 bpm, double bass, light, calm, drum kit, jazz</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task3/39.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task3/39.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task3/39.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>psychedelic rock, 110 bpm, guitar, positive, musical instrument</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task3/249.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task3/249.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task3/249.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>timpani, soundtrack, 125 bpm, soothing, acoustic, ambient</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task3/314.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task3/314.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task3/314.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>groove, acoustic, 125 bpm, dance, upbeat, happy, musical instrument</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task3/318.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task3/318.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task3/318.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  
</table>

---


[main]: static/image/Figure6.png

### Task 2: [Samples with single Prompts & Random Initial Noise]

#### Input Prompt 1: jazz, piano trio, swing, live recording feel, warm tone, improvisation

<table>
  <tr>
    <th>Sample</th>
    <th>Baseline</th>
    <th>CADS</th>
    <th>Ours</th>
  </tr>
  <tr>
    <td><b>Sample 1</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1114_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1114_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1114_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 2</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1114_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1114_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1114_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 3</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1114_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1114_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1114_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 4</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1114_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1114_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1114_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
</table>

#### Input Prompt 2: tropical house, drums, 105 bpm, animal, dance, piano

<table>
  <tr>
    <th>Sample</th>
    <th>Baseline</th>
    <th>CADS</th>
    <th>Ours</th>
  </tr>
  <tr>
    <td><b>Sample 1</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1120_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1120_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1120_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 2</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1120_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1120_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1120_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 3</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1120_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1120_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1120_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 4</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1120_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1120_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1120_6.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
</table>

#### Input Prompt 3: lofi, chill, vinyl noise, mellow, soft drums, warm chords, nostalgic

<table>
  <tr>
    <th>Sample</th>
    <th>Baseline</th>
    <th>CADS</th>
    <th>Ours</th>
  </tr>
  <tr>
    <td><b>Sample 1</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1115_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1115_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1115_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 2</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1115_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1115_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1115_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 3</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1115_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1115_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1115_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 4</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1115_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1115_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1115_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
</table>


#### Input Prompt 4: hopeful, mellow, acoustic

<table>
  <tr>
    <th>Sample</th>
    <th>Baseline</th>
    <th>CADS</th>
    <th>Ours</th>
  </tr>
  <tr>
    <td><b>Sample 1</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1121_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1121_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1121_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 2</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1121_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1121_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1121_4.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 3</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1121_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1121_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1121_8.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 4</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task1/1121_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task1/1121_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/task1/1121_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  
</table>

### Task 3: [Samples with various Prompts & Random Initial Noise]

#### Acoustic

<table>
  <tr>
    <th>Prompt</th>
    <th>Baseline</th>
    <th>CADS</th>
    <th>Ours</th>
  </tr>
  <tr>
    <td><b>acoustic, relax, guitar, plucked string instrument,105 bpm, popular, instrumental, echo, musical instrument, gentle</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/acoustic/306_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/acoustic/306_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/acoustic/306_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>hopeful, synthesizer, mellow, acoustic, 85 bpm</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/acoustic/309_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/acoustic/309_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/acoustic/309_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>relax, bass, acoustic, plucked string instrument, relaxed, musical instrument, contemplative</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/acoustic/311_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/acoustic/311_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/acoustic/311_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>piano, guitar, 85 bpm, zither, folk, acoustic, harp, musical instrument, sentimental, emotional</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/acoustic/313_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/acoustic/313_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/acoustic/313_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
</table>


#### Jazz

<table>
  <tr>
    <th>Prompt</th>
    <th>Baseline</th>
    <th>CADS</th>
    <th>Ours</th>
  </tr>
  <tr>
    <td><b>jazz,organ, piano, 110 bpm, emotional, musical instrument, romantic, nostalgic, longing, piano, organ, pizzicato, harp, heartfelt, moving</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/jazz/1_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/jazz/1_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/jazz/1_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>jazz,sad, piano, nostalgic, piano, melancholic, harp, gentle</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/jazz/3_5.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/jazz/3_5.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/jazz/3_5.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>110 bpm, easy, synthesizer, moving, jazz</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/jazz/4_6.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/jazz/4_6.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/jazz/4_6.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>jazz, soft, piano, piano, moving, emotional, peaceful, acoustic, melancholic, 110 bpm, calm, romantic, classical music, soulful</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/jazz/5_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/jazz/5_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/jazz/5_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>musical instrument, jazz, double bass, calm, solo, bowed string instrument, 110 bpm, sad, organ, melancholic, moving</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/jazz/7_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/jazz/7_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/jazz/7_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
</table>


#### Carol

<table>
  <tr>
    <th>Prompt</th>     
    <th>Baseline</th>     
    <th>CADS</th>     
    <th>Ours</th>
  </tr>
  <tr>
    <td><b>carol, christmas, calm, instrumental, 100 bpm, vibraphone, sad, musical instrument, guitar, piano, moving</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/carol/31_7.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/carol/31_7.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/carol/31_7.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>carol,musical instrument, guitar, calm, reflective, 100 bpm</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/carol/33_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/carol/33_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/carol/33_6.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>drums, moving, intimate, carol, 100 bpm, musical instrument, melancholic, speech, brass instrument, mellow</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/carol/35_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/carol/35_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/carol/35_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>guitar, ambient, bass, 100 bpm, ding, glockenspiel, moving,tinkle, jingle, mellow, carol, chill, relaxing</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/carol/37_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/carol/37_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/carol/37_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>warm, 100 bpm, harp, organ, carol</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/carol/38_4.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/carol/38_4.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/carol/38_4.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
</table>


#### Electronic

<table>
  <tr>
    <th>Prompt</th>     
    <th>Baseline</th>     
    <th>CADS</th>     
    <th>Ours</th>
  </tr>
  <tr>
    <td><b>upbeat, drum machine, electric piano, 125 bpm, dubstep</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/elec/92_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/elec/92_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/elec/92_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>electronic, zing, speech, drum and bass, a synthesizer, singing, 125 bpm</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/elec/93_8.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/elec/93_8.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/elec/93_8.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>upbeat, drum and bass, bass, musical instrument, aggressive, instrumental, sampler, electronic, cinematic, 125 bpm</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/elec/96_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/elec/96_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/elec/96_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>synthesizers, inspiring, 125 bpm, summer, spray, waterfall, electronic</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/elec/98_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/elec/98_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/elec/98_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
</table>


#### Electronic Pop

<table>
  <tr>
    <th>Prompt</th>     
    <th>Baseline</th>     
    <th>CADS</th>     
    <th>Ours</th>
  </tr>
  <tr>
    <td><b>110 bpm, passionate, boing, emotional, soulful, electronic pop, speech, love</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/elecpop/241_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/elecpop/241_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/elecpop/241_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>saturday night, boing, electronic pop, speech, double bass, 110 bpm, happiness, groovy, birthday, the synthesizer, piano, inside</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/elecpop/243_5.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/elecpop/243_5.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/elecpop/243_6.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>drums, guitar, acoustic, steel guitar, effects unit, bass, electronic pop, musical instrument, 110 bpm</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/elecpop/245_6.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/elecpop/245_6.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/elecpop/245_6.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>funky, guitar, speech, electronic pop, 110 bpm, positive, musical instrument, groovy, outside, boing, upbeat</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/elecpop/246_8.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/elecpop/246_8.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/elecpop/246_8.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>cool, funky, 110 bpm, musical instrument, electronic pop, rhythmical</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/elecpop/247_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/elecpop/247_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/elecpop/247_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
</table>


#### New Age

<table>
  <tr>
    <th>Prompt</th>     
    <th>Baseline</th>     
    <th>CADS</th>     
    <th>Ours</th>
  </tr>
  <tr>
    <td><b>115 bpm, piano, synthesizer, new-age music, cello, soft, electric piano</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/newage/181_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/newage/181_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/newage/181_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>115 bpm, tranquil, new-age music, moving, piano, strings, melancholic, lullaby, emotional</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/newage/182_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/newage/182_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/newage/182_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>emotional, new age, piano</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/newage/184_4.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/newage/184_4.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/newage/184_4.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>115 bpm, electric piano, reflective, harpsichord, emotional, calm, new age, moving, hopeful, piano, keyboard</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/newage/187_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/newage/187_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/newage/187_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>musical instrument, emotional, piano, moving, peaceful, reflective, relaxed, calm, speech, sentimental, electric piano, 115 bpm, new age</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/newage/189_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/newage/189_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/newage/189_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
</table>


#### Pop

<table>
  <tr>
    <th>Prompt</th>     
    <th>Baseline</th>     
    <th>CADS</th>     
    <th>Ours</th>
  </tr>
  <tr>
    <td><b>110 bpm, bass guitar, hip hop, pop, drums</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/pop/273_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/pop/273_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/pop/273_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>inspiring, pop, guitar, 110 bpm, musical instrument, acoustic guitar, dance</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/pop/276_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/pop/276_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/pop/276_4.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>positive, guitar, ding-dong, 110 bpm, pop, bass</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/pop/278_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/pop/278_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/pop/278_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>pop, electric guitar, bass guitar, synthesizer, 110 bpm, funky, plucked string instrument</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-Original/task2/pop/279_5.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SAO-CADS/task2/pop/279_5.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/pop/279_5.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
</table>

