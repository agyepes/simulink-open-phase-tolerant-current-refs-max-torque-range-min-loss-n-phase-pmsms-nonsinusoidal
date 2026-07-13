# Supplementary files for paper "Open-Phase-Tolerant Online Current References for Maximum Torque Range and Minimum Loss With Current and Torque-Ripple Limits for n-Phase Nonsalient PMSMs With Nonsinusoidal Back EMF"

This repository contains the open-access MATLAB/Simulink implementation and back-EMF lookup-table data associated with the method proposed in the following paper:

> A. G. Yepes, W. E. Abdel-Azim, A. Shawier, A. S. Abdel-Khalik, M. S. Hamad, S. Ahmed, and J. Doval-Gandoy, "Open-Phase-Tolerant Online Current References for Maximum Torque Range and Minimum Loss With Current and Torque-Ripple Limits for n-Phase Nonsalient PMSMs With Nonsinusoidal Back EMF," *IEEE Transactions on Transportation Electrification*, vol. 10, no. 1, pp. 432–449, March 2024, [doi:10.1109/TTE.2023.3288525](https://doi.org/10.1109/TTE.2023.3288525).

## Contents

| File | Description |
| --- | --- |
| `Proposed_method_Yepes2024TTE.slx` | Simulink implementation of the proposed online current-reference method, including the current-rms and torque-ripple limitation stages. |
| `angle.mat` | Electrical-angle samples for one period of the normalized back-EMF lookup table. The variable stored in the file is `angle`. |
| `backEMF.mat` | Normalized back-EMF samples corresponding to `angle`. The variable stored in the file is `backEMF`. |
| `README.md` | Description, usage instructions, provenance, integrity information, and related resources. |
| `LICENSE.txt` | CC BY 4.0 license and attribution information. |
| `CITATION.cff` | Machine-readable software and associated-paper citation metadata. |

The model implements the overall method represented in Fig. 6 of the paper. Its named subsystems include the torque-ripple limitation of Fig. 10 and the current-rms limitation of Fig. 14. The lookup-table data support the normalized nonsinusoidal back-EMF representation discussed with Fig. 17.

## Requirements and compatibility

- MATLAB
- Simulink
- Stateflow

The model was saved with MATLAB/Simulink R2016a. The exact files in this repository were also load-tested, without modification or resaving, in MATLAB/Simulink R2026a.

## How to use

1. Download or clone the repository, keeping `Proposed_method_Yepes2024TTE.slx`, `angle.mat`, and `backEMF.mat` in the same folder.
2. Set that folder as the current MATLAB folder.
3. Open `Proposed_method_Yepes2024TTE.slx`.
4. Run the model.

The model initialization callback automatically loads `angle.mat` and `backEMF.mat`. The supplied configuration uses a fixed-step discrete solver and a default stop time of 30 s.

## Provenance and corrections

The three technical files are byte-for-byte identical to the corresponding files in both:

- the [supplementary archive published through IEEE Xplore](https://ieeexplore.ieee.org/ielx7/6687316/10473608/10159366/tte-3288525-mm.zip?arnumber=10159366); and
- the [supplementary archive shared on ResearchGate](https://www.researchgate.net/publication/374630807).

The documentation accompanying the original IEEE Xplore archive contains outdated metadata, including an earlier model filename and an incorrect paper year. This repository and the corrected ResearchGate package provide updated `README.md`, `LICENSE.txt`, and `CITATION.cff` while leaving the three technical MATLAB/Simulink files unchanged.

### SHA-256 checksums

| File | SHA-256 |
| --- | --- |
| `Proposed_method_Yepes2024TTE.slx` | `eb329db848312d2f78dffe04870e97bb33eb3c12536d4f5b12620b9313c4696b` |
| `angle.mat` | `3d2ac59903c08a8ccf5d6c17d05dede84ae1c52b1c296d9e0efb54a19b3a73f1` |
| `backEMF.mat` | `2dd4571dfb792a944fbec812bcb1ba89a0265bf56910df91b5d072399efefeae` |

For reference, the complete IEEE wrapper archive downloaded during preparation had SHA-256 `81eec26f4f5753909e14842bbe2ae386ad55d568f87347111bcadc144cffb3b4`. The corrected ResearchGate archive has SHA-256 `5534e66bc53af37e44d4dac262cb977e7ca5e8d66bcc743cf1428ad7102fb71c`. Their packaging differs, but their three technical files match exactly.

## Related resources

- Paper: https://doi.org/10.1109/TTE.2023.3288525
- Zenodo software record: https://doi.org/10.5281/zenodo.21345273
- IEEE Xplore supplementary material: https://ieeexplore.ieee.org/abstract/document/10159366/media
- ResearchGate supplementary-material record: https://www.researchgate.net/publication/374630807
- Related Simulink tutorial 1: https://www.youtube.com/watch?v=vQROHWiQqzo
- Related Simulink tutorial 2: https://www.youtube.com/watch?v=FIbG3naupD4
- Related tutorial playlist: https://www.youtube.com/playlist?list=PLk8b_j0g3ncehqksxd8hzFtUyFdBzhgOk

The two videos demonstrate changes of current-reference scenarios in the earlier conference-version model related to this work; they are not recordings of the exact TTE supplementary file in this repository.

## License

Unless otherwise stated, the files in this repository are licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0). See `LICENSE.txt` for details.

## Citation

Please cite the associated IEEE TTE paper above when using these files. When citing this archived software release, use https://doi.org/10.5281/zenodo.21345273. A machine-readable citation is provided in `CITATION.cff`.
