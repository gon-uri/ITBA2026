# Notebook

`ml_neural_ts_notebook.ipynb` is the hands-on notebook of the lecture *Machine learning for neural time series*
(ITBA, 23 October 2026). It runs top to bottom in Google Colab on the free CPU, with no code to write:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gon-uri/ITBA2026/blob/main/notebook/ml_neural_ts_notebook.ipynb)

- **EEG, eyes open vs closed** (PhysioNet EEGBCI, 20 people): look at the spectra (§1); PREDICT with one feature vs
  the whole spectrum, tested on new people, and what happens when windows of the same person leak into the test set
  (§2); REPRESENT with t-SNE and k-means (§3); PREDICT with random features: MiniRocket on the raw signal of three
  back-of-head electrodes, against their hand-made spectrum (§4).
- **fMRI, child vs adult** (nilearn development dataset, 155 people): classify from the brain connectome, with
  balanced accuracy and a head-motion check (§6); predict age (§7).
- **At home:** four open questions and links to go further.

Section numbers follow the lecture slides, so there is no §5.

The first cell installs only `mne==1.11.0`, `nilearn==0.13.1` and `aeon==1.6.0` (pinned so that Colab does not ask
for a restart). The EEG is downloaded from the AWS copy of PhysioNet (with `data/eoec_features.npz` as a fallback) and
the fMRI file from `data/` of this repository, each checked by its checksum. The notebook is saved with its outputs, so
every result can also be read without running it.
