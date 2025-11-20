---
layout: default
title: Lishan Li | Phonetics & Computation
description: "Decoding the melody of speech with data."
---

# Lishan Li (李丽珊)

<div style="display: flex; align-items: center; gap: 20px;">
  <img src="https://avatars.githubusercontent.com/u/9919?s=200&v=4" alt="Lishan Li" style="border-radius: 50%; width: 150px; height: 150px; object-fit: cover; border: 2px solid #333;">
  <div>
    <p><strong>Research Assistant @ Beijing Normal University</strong></p>
    <p>
      Focus: <code>Phonetics</code> <code>Tone Perception</code> <code>Dialectology</code> <code>CompLing</code>
    </p>
    <p>📍 Beijing, China | 📧 <a href="mailto:lilishan0121@gmail.com">lilishan0121@gmail.com</a></p>
  </div>
</div>

---

### 👋 About Me

I am a linguistics researcher decoding the **melody of speech**.

My work bridges the gap between **fieldwork** (recording 180+ children; documenting endangered dialects) and **computational modeling** (Python/R pipelines). I am particularly interested in how tones merge over time and how linguistic tones interact with musical melodies.

[cite_start]Currently, I am a full-time Research Assistant at the **School of Chinese Language and Literature, BNU**[cite: 38], working with Prof. Xiaoying Xu.

* [cite_start]**M.A.** in Chinese Linguistics, Beijing Normal University (2025) - *Outstanding Graduate* [cite: 5, 84]
* [cite_start]**B.A.** in Chinese Linguistics, Shandong University (2022) - *Rank 6/102* [cite: 11, 13]

---

### 🔥 News

* **[Sep 2025]** Started full-time position as Research Assistant at BNU.
* **[Aug 2025]** Oral presentation at **Interspeech 2025** on Cantonese Tone Merging! [cite_start]🎤 [cite: 28]
* [cite_start]**[Jun 2025]** Graduated from BNU with the "Outstanding Graduate of Beijing" award. [cite: 83]
* [cite_start]**[Dec 2024]** Paper on dialect loss and tone perception published in **JASA** (Vol. 156). [cite: 21, 22]

---

### 📝 Selected Publications

#### 2025
* **Lexical competition in the process of Cantonese tone merging: Diverse Impact Mechanisms**
    * **Li, L.**, Zhou, Y., & Xu, X.
    * *In Proc. of Interspeech 2025* (**Oral Presentation**)
    * [📄 PDF] [💻 Code]

* **Level-Tone Merger in Production and Perception: Study in two Chinese Min Dialects**
    * Wu, Y., **Li, L.**, & Xu, X.
    * [cite_start]*IALP 2025* (*Equal Contribution*) [cite: 29]

#### 2024
* **The influence of dialect loss on tone perception: Diminishing voice quality cues**
    * Zhang, Y., **Li, L.**, Lai, W., & Xu, X.
    * *Journal of the Acoustical Society of America (JASA)*, 156(6):3707-3722.
    * [📄 Paper Link]

---

### 💻 The "Geek" Side

I don't just analyze data; I visualize the invisible sound.

```python
# A glimpse into my daily work:
# Visualizing Tone Contours with Python (Matplotlib & Parselmouth)

import parselmouth
import matplotlib.pyplot as plt

def plot_pitch(sound_file):
    snd = parselmouth.Sound(sound_file)
    pitch = snd.to_pitch()
    pitch_values = pitch.selected_array['frequency']
    
    plt.figure(figsize=(10, 4))
    plt.plot(pitch.xs(), pitch_values, 'o', markersize=2, color='w')
    plt.plot(pitch.xs(), pitch_values, '-', color='#4e79a7') # My favorite blue
    plt.title("The Shape of a Cantonese Tone")
    plt.ylabel("Frequency (Hz)")
    plt.grid(False)
    plt.show()

# [cite_start]Current Status: Analyzing 2,000+ Folk Songs [cite: 54]
