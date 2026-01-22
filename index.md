---
layout: project_page
permalink: /

title: PADS-TAL Padding Annealed Diffusion Sampling in Text Aligned Latent for Robust and Diverse Text-to-Music Generation
authors:
    anonymous
affiliations:
    anonymous
paper: https://www.cs.virginia.edu/~robins/Turing_Paper_1936.pdf
video: https://www.youtube.com/results?search_query=turing+machine
code: https://github.com/topics/turing-machines
data: https://huggingface.co/docs/datasets
---

<!-- Using HTML to center the abstract -->
<div class="columns is-centered has-text-centered">
    <div class="column is-four-fifths">
        <h2>Abstract</h2>
        <div class="content has-text-justified">
Text-to-Music (T2M) diffusion models increasingly adopt Transformer backbones (DiT), 
yet practical deployments often rely on short tag-style prompts and face persistent challenges: generations can collapse to limited patterns, while controlling diversity at inference time remains difficult under strict semantic requirements. Training-free sampling methods like CADS, while effective in Text-to-Image, can severely degrade alignment and fidelity in TTM because early-timestep perturbations strongly alter global musical attributes (e.g., genre, mood, structure). We propose two complementary solutions: Padding Annealed Diffusion Sampling (PADS), which injects timestep-dependent noise only into padding tokens while freezing semantic tokens to prevent semantic drift, and Text-Aligned Latent (TAL), a text-aware latent space learned via a redesigned VAE so diffusion sampling occurs near text-consistent neighborhoods. Together, PADS+TAL improve diversity while preserving prompt-aligned global attributes in TTM.
        </div>
    </div>
</div>


<img src="static/image/Figure11.png">


## Audio Examples

### Task 1: [Text-to-Music Generation with single Prompts]

#### Input Prompt 1: jazz, piano trio, swing, live recording feel, warm tone, improvisation

<table>
  <tr>
    <th>Sample</th>
    <th>Baseline</th>
    <th>CADS</th>
    <th>Ours (PADS)</th>
  </tr>
  <tr>
    <td><b>Sample 1</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/task1/1114_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1114_0.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/task1/1114_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1114_1.mp3" type="audio/mpeg">
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
    <td><b>Sample 3</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/task1/1114_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1114_2.mp3" type="audio/mpeg">
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
    <td><b>Sample 4</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/task1/1114_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1114_3.mp3" type="audio/mpeg">
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

#### Input Prompt 2: lofi, chill, vinyl noise, mellow, soft drums, warm chords, nostalgic

<table>
  <tr>
    <th>Sample</th>
    <th>Baseline</th>
    <th>CADS</th>
    <th>Ours (PADS)</th>
  </tr>
  <tr>
    <td><b>Sample 1</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/task1/1115_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1115_0.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/task1/1115_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1115_1.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/task1/1115_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1115_2.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/task1/1115_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1115_3.mp3" type="audio/mpeg">
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

#### Input Prompt 3: tropical house, drums, 105 bpm, animal, dance, piano

<table>
  <tr>
    <th>Sample</th>
    <th>SA-Original</th>
    <th>SA-CADS</th>
    <th>TAL-PADS (Ours)</th>
  </tr>
  <tr>
    <td><b>Sample 1</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/task1/1120_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1120_0.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/task1/1120_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1120_1.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/task1/1120_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1120_2.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/task1/1120_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1120_3.mp3" type="audio/mpeg">
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

#### Input Prompt 4: hopeful, mellow, acoustic

<table>
  <tr>
    <th>Sample</th>
    <th>SA-Original</th>
    <th>SA-CADS</th>
    <th>TAL-PADS (Ours)</th>
  </tr>
  <tr>
    <td><b>Sample 1</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/task1/1121_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1121_0.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/task1/1121_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1121_1.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/task1/1121_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1121_2.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/task1/1121_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/task1/1121_3.mp3" type="audio/mpeg">
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

### Task 2: [Text-to_Music Generation with Genre-wised Multi Prompts]

#### Acoustic

<table>
  <tr>
    <th>Prompt</th>
    <th>SA-Original</th>
    <th>SA-CADS</th>
    <th>TAL-PADS (Ours)</th>
  </tr>
  <tr>
    <td><b>relaxing, background music, ambient, instrumental, tick-tock, acoustic,pizzicato, cinematic, zither</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/acoustic/302_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/acoustic/302_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/acoustic/302_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>acoustic, relax, guitar, plucked string instrument,105 bpm, popular, instrumental, echo, musical instrument, gentle</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/acoustic/306_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/acoustic/306_0.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/acoustic/309_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/acoustic/309_1.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/acoustic/311_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/acoustic/311_1.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/acoustic/313_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/acoustic/313_1.mp3" type="audio/mpeg">
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
    <th>SA-Original</th>
    <th>SA-CADS</th>
    <th>TAL-PADS (Ours)</th>
  </tr>
  <tr>
    <td><b>jazz,organ, piano, 110 bpm, emotional, musical instrument, romantic, nostalgic, longing, piano, organ, pizzicato, harp, heartfelt, moving</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/jazz/1_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/jazz/1_1.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/jazz/3_5.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/jazz/3_5.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/jazz/4_6.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/jazz/4_6.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/jazz/5_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/jazz/5_0.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/jazz/7_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/jazz/7_9.mp3" type="audio/mpeg">
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
    <th>SA-Original</th>
    <th>SA-CADS</th>
    <th>TAL-PADS (Ours)</th>
  </tr>
  <tr>
    <td><b>carol, christmas, calm, instrumental, 100 bpm, vibraphone, sad, musical instrument, guitar, piano, moving</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/carol/31_7.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/carol/31_7.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/carol/33_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/carol/33_1.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/carol/35_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/carol/35_3.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/carol/37_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/carol/37_2.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/carol/38_4.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/carol/38_4.mp3" type="audio/mpeg">
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
    <th>SA-Original</th>
    <th>SA-CADS</th>
    <th>TAL-PADS (Ours)</th>
  </tr>
  <tr>
    <td><b>upbeat, drum machine, electric piano, 125 bpm, dubstep</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/elec/92_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/elec/92_9.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/elec/93_8.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/elec/93_8.mp3" type="audio/mpeg">
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
    <td><b>vocal samples, sports, synthesizer, 125 bpm, drum machine, buzz, electronic music, electronic</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/elec/94_4.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/elec/94_4.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/elec/94_4.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>upbeat, drum and bass, bass, musical instrument, aggressive, instrumental, sampler, electronic, cinematic, 125 bpm</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/elec/96_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/elec/96_3.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/elec/98_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/elec/98_1.mp3" type="audio/mpeg">
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
    <th>SA-Original</th>
    <th>SA-CADS</th>
    <th>TAL-PADS (Ours)</th>
  </tr>
  <tr>
    <td><b>110 bpm, passionate, boing, emotional, soulful, electronic pop, speech, love</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/elecpop/241_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/elecpop/241_1.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/elecpop/243_5.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/elecpop/243_5.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/elecpop/245_6.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/elecpop/245_6.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/elecpop/246_8.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/elecpop/246_8.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/elecpop/247_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/elecpop/247_1.mp3" type="audio/mpeg">
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
    <th>SA-Original</th>
    <th>SA-CADS</th>
    <th>TAL-PADS (Ours)</th>
  </tr>
  <tr>
    <td><b>115 bpm, piano, synthesizer, new-age music, cello, soft, electric piano</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/newage/181_2.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/newage/181_2.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/newage/182_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/newage/182_9.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/newage/184_4.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/newage/184_4.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/newage/187_3.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/newage/187_3.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/newage/189_0.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/newage/189_0.mp3" type="audio/mpeg">
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
    <th>SA-Original</th>
    <th>SA-CADS</th>
    <th>TAL-PADS (Ours)</th>
  </tr>
  <tr>
    <td><b>speech, guitar, acoustic guitar, trap, instrumental, drums, love, 110 bpm, steel guitar, musical instrument, playful, relaxing</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/pop/272_6.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/pop/272_6.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL-PADS/pop/272_6.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>110 bpm, bass guitar, hip hop, pop, drums</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-Original/pop/273_1.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/pop/273_1.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/pop/276_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/pop/276_9.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/pop/278_9.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/pop/278_9.mp3" type="audio/mpeg">
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
        <source src="static/audio_samples/SA-Original/pop/279_5.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/SA-CADS/pop/279_5.mp3" type="audio/mpeg">
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



---


[main]: static/image/Figure6.png
