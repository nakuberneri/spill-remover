# Spill Remover

Remove microphone spill (also called bleed or leakage) from a track using an isolated recording of the source that spills into it (a DI, a click track, a close mic).

Load the track to clean and the reference, pick a strength, listen to original / cleaned / removed, and download the cleaned WAV. Everything runs in the browser; no audio is uploaded.

## How it works

1. **Linear stage** – estimates the transfer function from the reference to the target mic over the whole file (level, EQ, delay, polarity, room) and subtracts the predicted spill.
2. **Spectral stage** (Medium / Strong) – a gentle spectral gate on the residual, driven by the spill estimate.

Works best when the reference contains none of the instrument you want to keep and the path from source to mic is stable.

## Use

Open `index.html` in any modern browser, or host it with GitHub Pages.
