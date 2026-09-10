# Childhood Climate Exposure and Adult Brain Connectivity

An exploratory, fully reproducible analysis asking whether childhood temperature exposure
(ages 6–16) leaves a trace in adult prefrontal cortex (PFC) structural connectivity.

**Short answer: no.** Using a real, verified 250-year historical weather record and N=86
participants, we found no statistically supported association, across eight independent
robustness checks (VIF, alternative model setups, age-residualization, HC3-robust inference,
permutation testing, a zero-inclusive connectivity definition, multiple-comparison correction,
and a five-year anchor-year sensitivity analysis).

This repository also documents something more interesting than the null result itself: an
earlier development version of this pipeline, run on a placeholder weather series (built by
hand before the real data was obtained), briefly produced a "significant" result. That result
did not survive the same robustness checks and disappeared completely once the real,
verified climate record was used. The full manuscript reports this sequence openly, as a
concrete demonstration of why both rigorous sensitivity analysis and verifying real data
sources matter before reporting a finding.

## What's in this repository

| Folder | Contents |
|---|---|
| `manuscript/` | Full write-up: background, methods, results, discussion, limitations |
| `notebook/` | Complete analysis pipeline, from raw data to every reported statistic |
| `data/` | All input data needed to reproduce every result |
| `figures/` | The two figures referenced in the manuscript |

## Reproducing the analysis

1. Download everything in `data/` into the same folder as the notebook.
2. Open `notebook/neuro_climatology_analysis.ipynb` in Jupyter or Google Colab.
3. Run all cells top to bottom.

The notebook will refuse to run if `prague_klementinum_annual.csv` (the real climate data) is
missing — it does not fall back to placeholder data, on purpose.

## Data sources

- **Structural connectivity:** Škoch A, Rehák Bučková B, Mareš J, et al. Human brain structural
  connectivity matrices: ready for modelling. *Sci Data*, 9: 486, 2022. Publicly available,
  de-identified.
- **Climate record:** European Climate Assessment & Dataset (ECA&D), Praha-Klementinum
  station (STAID 27), https://www.ecad.eu.

## Citation

If you use this pipeline or build on this analysis, please cite the manuscript in
`manuscript/` (full citation to be added once published) and acknowledge the original data
sources above.

## License

[Optional — e.g., MIT for code, or "All rights reserved" until the manuscript is published.
Add a LICENSE file if you choose one.]
