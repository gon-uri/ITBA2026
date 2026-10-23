# Notebook

`ml_neural_ts_notebook.ipynb` is the hands-on notebook of the lecture *Machine learning for neural time series*
(ITBA, 23 October 2026). It runs top to bottom in Google Colab on the free CPU, with no code to write:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gon-uri/ITBA2026/blob/main/notebook/ml_neural_ts_notebook.ipynb)

- **In class (§0–§8):** EEG eyes open vs closed (PhysioNet EEGBCI, 20 people) — predict, represent, connect, and how
  much the test split matters; fMRI child vs adult from brain connectomes, with a head-motion check, and age
  regression.
- **At home (Part B):** rat hippocampal place cells, decoding objects from fMRI (Haxby), clustering sleep, a
  Riemannian EEG model, leakage and luck on pure noise, logistic regression trained by gradient descent; then extra
  exercises.

The first cell installs only `mne==1.11.0` and `nilearn==0.13.1` (pinned so that Colab does not ask for a restart).
The EEG is downloaded from the AWS copy of PhysioNet, the other files from `data/` of this repository, each checked by
its checksum. The notebook is saved with its outputs, so every result can also be read without running it.
