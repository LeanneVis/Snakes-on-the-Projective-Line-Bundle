# Snakes-on-the-Projective-Line-Bundle

This repository contains code to segment (synthetic) SEM images on the projective line bundle $\mathbb{R}^2 \times P^1$.

# Requirements
- Mathematica / Wolfram Language

- Input image file (000040_32.0_CD_32.0_H_45.0.png)

- Precomputed geodesic tracking results (Synthetic_cd16_height40_00.h5 and Synthetic_cd16_height40_20.h5)

# Description/ Instructions
To reproduce the experiment, run the Mathematica notebook:
spatialsnakes.nb

The notebook contains the following steps:
1. **Loads the input image:** 000040_32.0_CD_32.0_H_45.0.png

2. **Loads the precomputed geodesic tracking data:** Synthetic_cd16_height40_00.h5 and Synthetic_cd16_height40_20.h5

The geodesic tracking results are computed using the implementation provided by Finn Sherry, available at:
https://github.com/finnsherry/IterativeEikonal
This implementation corresponds to the method described in the following paper:

N.J. van den Berg, F.M. Sherry, T.T.J.M. Berendschot, and R. Duits,
Crossing-Preserving Geodesic Tracking on Spherical Images,
10th International Conference on Scale Space and Variational Methods in Computer Vision (SSVM), 2025.
https://doi.org/10.1007/978-3-031-92369-2_15

Running the notebook produces the following output files:
1. **Connected-component-informed cost function used for geodesic tracking:** CSE2EdgesCC.hdf5

2. **Sink and target point sets for the geodesic tracking:** sinksandtargets.hdf5

These output files can be used as input for the geodesic tracking code provided by Finn Sherry in the IterativeEikonal repository.

# Acknowledgements & Citation
If you use this code in your own work, please cite our paper:

[1] Vis, L. and Pisarenco, M. and Smets, B.M.N. and van der Sommen, F and Duits, R. "Sub-Riemannian Snakes on the Projective Line Bundle with Applications to Segmentation of SEM Images." arXiv print: https://doi.org/....

```
@article{Vis2026Snakes,
  author =       {Vis, Leanne and Pisarenco, Maxim and Smets, Bart M.N. and van der Sommen, Fons and Duits, Remco},
  title =        {{Sub-Riemannian Snakes on the Projective Line Bundle with Applications to Segmentation of SEM Images}},
  publisher =    {arXiv preprint},
  year =         {2026},
  doi =          {10.}
}
```
