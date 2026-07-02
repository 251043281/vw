:::: {.columns}
::: {.column width="50%"}

## Presentation Title
#### Yip Jia Xin
#### Matric No: 251043281
#### UR6527001 - Materials Engineering
#### Universiti Malaysia Perlis

<audio id="bg-music" src="media/audio/sb.m4a" loop></audio>

<div id="audio-credit"
     style="position: absolute; bottom: 40px; right: 20px; font-size: 0.6em; opacity: 0.6;">
  Music: “Adrift” by Scott Buckley (CC BY 4.0)
</div>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const audio = document.getElementById('bg-music');
    const credit = document.getElementById('audio-credit');

    // hide credit by default
    credit.style.display = 'none';

    const test = new Audio('media/audio/bgm.mp3');

    test.addEventListener('canplaythrough', () => {
      // bgm.mp3 exists → use it, keep credit hidden
      audio.src = 'media/audio/bgm.mp3';
    }, { once: true });

    test.addEventListener('error', () => {
      // bgm.mp3 missing → sb.m4a will play → show credit
      credit.style.display = 'block';
    }, { once: true });

    document.addEventListener('click', () => {
      if (Reveal.getIndices().h === 0) {
        audio.volume = 0.5;
        audio.play();
      }
    }, { once: true });

    Reveal.on('slidechanged', (event) => {
      if (event.indexh > 0) { audio.pause(); }
      else { audio.play(); }
    });
  });
</script>

:::

::: {.column width="50%"}
![](media/pics/logo1.png)
:::

::::

---

:::: {.columns}
::: {.column width="50%"}

## Resistance Analysis (Machine 1)

This visualization examines the interplay between **Temperature** and **Pressure** on the resulting **PartResistance**.

- **Machine Focus**: Data is filtered exclusively for Machine 1.
- **Trend Observation**: Higher temperatures often correlate with variations in resistance, potentially amplified by pressure shifts.
- **Significance**: Understanding these parameters is critical for maintaining material quality in Engineering.

:::

::: {.column width="50%"}
<iframe data-src='media/plots/resistance_analysis.html' width='100%' height='500px' style='border:none;'></iframe>
:::

::::

---

:::: {.columns}
::: {.column width="50%"}

## Effects of Pressure (Machine 1)

Analysis of the impact of **Pressure** on **PartResistance**:

- **Significance**: The statistical test yielded a p-value of **0.0000**.
- **Quality Standard**: Target is below USL = 10 $\Omega$.
- **Conclusion**: Pressure shifts significantly influence the variance in resistance, impacting material consistency.

:::

::: {.column width="50%"}
<iframe data-src='media/plots/pressure_effect.html' width='100%' height='500px' style='border:none;'></iframe>
:::

::::

---

:::: {.columns}
::: {.column width="50%"}

## Effects of Temperature (Machine 1)

Analysis of the impact of **Temperature** on **PartResistance**:

- **Significance**: The statistical test yielded a p-value of **0.0000**.
- **Optimization**: Increasing the temperature generally reduces part resistance, supporting the "lower is better" objective.
- **Conclusion**: Temperature acts as a critical process variable.

:::

::: {.column width="50%"}
<iframe data-src='media/plots/temp_effect.html' width='100%' height='500px' style='border:none;'></iframe>
:::

::::

---



---

---
# Bibliography
<div id="refs"></div>
