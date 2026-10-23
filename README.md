# Machine learning for neural time series — ITBA, 23 October 2026

Material for an invited lecture by **Gonzalo Uribarri** (Stockholm University) at ITBA (Instituto Tecnológico de
Buenos Aires), in a neuroscience course.

**Topics:** what makes a time series different from other data; the tasks we ask of neural time series
(classification, forecasting, embedding, clustering, inferring a graph); strategies for EEG/MEG, fMRI and spike
data; and how to check that a model really learned what we think it learned.

## Contents

| Path | What |
|---|---|
| `notebook/` | The Google Colab notebook for the hands-on part (added before the lecture) |
| `data/` | Small, precomputed data files the notebook downloads (see below) |

## Data files and licences

All files are derived from open datasets. If you reuse them, cite the original sources and keep their licences.

| File | Size | Derived from | Licence |
|---|---|---|---|
| `eoec_features.npz` | 14.9 MB | PhysioNet EEG Motor Movement/Imagery (EEGBCI), runs 1–2 (eyes open / closed), subjects 1–20, processed as in the lecture: log power spectra (1–40 Hz, 64 channels) of the 1,200 2-s windows with labels, person ids, channel names and positions; per-person alpha (8–12 Hz) envelope-correlation matrices; the continuous Oz signal after the 1–40 Hz filter and the unfiltered O1, Oz, O2 and Fp1 signals of every recording. Schalk et al. 2004, IEEE TBME 51(6):1034, doi:10.1109/TBME.2004.827072; Goldberger et al. 2000 (PhysioNet) | ODC-By 1.0 |
| `sleep8_feat.npz` | 0.3 MB | Sleep-EDF Expanded, Sleep Cassette, 8 nights: relative band power of 30-s epochs (Fpz-Cz, Pz-Oz) + hypnogram labels. Kemp et al. 2000, IEEE TBME 47(9):1185, doi:10.1109/10.867928 | ODC-By 1.0 |
| `fmri_development_msdl.npz`, `fmri_development_msdl_nolowpass.npz` | 3.9 MB each | fMRI of 155 children and adults watching a short movie (Richardson et al. 2018, Nat Commun 9:1027, doi:10.1038/s41467-018-03399-2; OpenNeuro ds000228), preprocessed version distributed with nilearn: MSDL atlas region time series, head motion, age | CC BY 4.0 |
| `fmri_haxby_subj2_vt.npz` | 2.5 MB | Haxby et al. 2001, Science 293:2425 (subject 2, ventral temporal cortex voxels, via PyMVPA / nilearn) | CC BY-SA 3.0 (this derived file keeps the same licence) |
| `achilles_dandi000044_maze_25ms.npz` | 1 MB | Rat hippocampus CA1 place cells (Grosmark & Buzsáki 2016, Science 351:1440; DANDI archive 000044), 25-ms binned spike counts and position | CC BY 4.0 |

SHA-256 checksums (used by the notebook to verify downloads):

```
48564036f85d8feddb2f791d69da78fb12d17be23f114d61721c5221f16731cf  eoec_features.npz
c518551bc668be8b5c681fc53e55504b11fbb45f2dbf5ad8f8a007c8c19a2bd1  sleep8_feat.npz
9cf96e73b8a8ba1034d32e7f96fc75b9142f1acf3e992ea349d8dabbbdb01518  fmri_development_msdl.npz
3efb101ff12b6dd245b48f917f60b7cebb377c64acaf27561ead4acfbe826c97  fmri_development_msdl_nolowpass.npz
468c1605c0cba2974f286a8f7691df4fdb619ef89b6712f9a631ff135e7d8cb4  fmri_haxby_subj2_vt.npz
77585aba3306072d205a323755bb0fffb32a0a441e81a116d4c400567bc33413  achilles_dandi000044_maze_25ms.npz
```

## Code licence

Code in this repository (the notebook) is released under the MIT licence (`LICENSE`). Data files keep the
licences listed above.
