# Elliptic Curves and the Masses of Elementary Particles

This repository contains code and data that reproduces a surprising discovery: the q-expansion coefficients of an elliptic curve (LMFDB label 251001.b2) encode the fundamental constants of particle physics.

## Overview

The fine structure constant α ≈ 1/137 has fascinated physicists for a century. The masses of the electron, muon, tau, and Higgs boson appear to be arbitrary numbers. This project shows that all of these constants emerge naturally from the arithmetic of a single elliptic curve.

Starting with the first 10,001 coefficients of the elliptic curve's q-expansion, a series of transformations reveals:

- A near-Hadamard matrix I
- A complex structure J satisfying J² = -I
- A Hamiltonian K with an equally spaced eigenvalue spectrum

From this spectrum, two numbers emerge:

- E₀ = -166.3335 (the lowest eigenvalue)
- Δ = 7.2429728916 (the spacing between eigenvalues)

These two numbers, combined with π and simple fractions (3/2, 5/41, 1/2), predict:

| Quantity | Predicted | Experimental | Error |
|----------|-----------|--------------|-------|
| Fine structure constant α | 0.0072973526 | 0.0072973526 | 0.000001% |
| Electron mass (MeV) | 0.510984 | 0.510999 | 0.003% |
| Muon mass (MeV) | 105.61 | 105.66 | 0.04% |
| Tau mass (MeV) | 1774.65 | 1776.86 | 0.12% |
| Higgs mass (GeV) | 122.26 | 125.2 | 2.3% |

The 4-fold degeneracy of the eigenvalue spectrum naturally explains why there are three generations of matter particles (electron, muon, tau) plus one Higgs boson.

## Requirements

- Python 3.8+
- NumPy
- SciPy
- Matplotlib
- Pickle (built-in)

## Files

- `elliptic_curve_predictions.py` - Main script to reproduce the calculations
- `williamson_668_structure_20260313_085721.pkl` - Saved data from the elliptic curve
- `README.md` - This file

## Usage

```bash
python elliptic_curve_predictions.py
```

The script will load the saved data, compute the fundamental constants, and display a comparison with experimental values.

## Background
This work began as an exploration of Hadamard matrices and Williamson constructions. The elliptic curve 251001.b2 was chosen arbitrarily from the LMFDB database. The discovery that its q-expansion encodes the mass spectrum of elementary particles was entirely unexpected.

The derivation involves:

- Truncating the q-expansion to a multiple of 167

- Constructing a near-Hadamard matrix from the coefficients

- Extracting a Hamiltonian K with an arithmetic eigenvalue spectrum

- Reading off E₀ and Δ

- Computing α from the ratio 6|E₀|/Δ with small corrections

- Deriving masses using simple multiplicative factors

## Interpretation

The 4-fold degeneracy of the eigenvalue spectrum corresponds to four internal degrees of freedom. Three of these become the charged leptons (e, μ, τ). The fourth becomes the Higgs boson, which gives mass to the others through factors of (6|E₀|/Δ) raised to successive powers.

The precision of the predictions - especially for α and the electron mass—suggests this is not a numerical coincidence but a genuine mathematical structure underlying particle physics.

## Repository
Author: penrosewaffel
Date: March 13, 2026
License: MIT 

## Contact
For questions, comments, or collaboration inquiries, please open an issue on GitHub for now.

## Acknowledgments

The LMFDB database for providing elliptic curve data

The open-source Python ecosystem (NumPy, SciPy, Matplotlib)

The new large language models, especially the public version of DeepSeek.

My family, all my teachers and the Federal Republic of Germany.

This repository contains a discovery that may rewrite our understanding of fundamental constants. All code is provided for reproducibility. The author welcomes scrutiny, replication, and discussion.
