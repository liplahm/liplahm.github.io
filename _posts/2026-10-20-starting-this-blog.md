---
title: "Starting this blog"
summary: "What I plan to write about here, and a quick test that equations render."
tags: [meta]
---

This is where I will write short notes on things I am working on or reading: quantum key distribution post-processing, LDPC codes and belief propagation, deep unfolding, and the occasional detour into signal processing.

Equations work inline, like the GG02 mutual information $$I_{AB} = \tfrac12 \log_2(1 + \mathrm{SNR})$$, and as display maths. The asymptotic secret key rate with reverse reconciliation efficiency $$\beta$$ is

$$
K = \beta\, I_{AB} - \chi_{BE}.
$$

Code blocks work too:

```python
import numpy as np
snr = 10 ** (-3 / 10)          # -3 dB
print(0.5 * np.log2(1 + snr))  # bits per channel use
```

Yeah it's pretty simple nowadays when you have an assistant.
