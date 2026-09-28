# Mathematical Methods for Machine Learning

**A rigorous, self-contained compendium: from real analysis to stochastic differential equations.**

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![PDF](https://img.shields.io/badge/PDF-335%20numbered%20pages-blue.svg)](pdf/mathematical-methods-for-ml.pdf)
[![Status](https://img.shields.io/badge/status-living%20document-brightgreen.svg)](#status-and-versioning)
[![Made with LaTeX](https://img.shields.io/badge/made%20with-LaTeX-008080.svg)](src/)

📄 **[Download the PDF](pdf/mathematical-methods-for-ml.pdf)** · 🐛 [Report an error](../../issues) · 🤝 [Contribute](CONTRIBUTING.md) · 📎 [Cite this work](CITATION.cff)

---

## Overview

*Mathematical Methods for Machine Learning* develops a unified pathway from the foundations of mathematical analysis to the advanced methods used for modeling and inference. It covers calculus, linear and functional analysis, differential equations, optimization, Fourier methods, and probability, together with the operational tools needed for biophysical modeling and probabilistic inference in complex systems.

The compendium contains 335 numbered pages (342 physical pages including front matter and table of contents) across 12 chapters, each split into several source files. It began in June 2023 as a study companion to the Analysis course taught by Prof. Monica Conti at Politecnico di Milano. It has since grown into a much broader treatment, last updated in September 2026.

Every result is developed with its assumptions stated, its proof (or a proof sketch) given, and its role in modern machine learning and computational neuroscience made explicit.

## Why this exists

I am a Medtech student at Campus Bio-Medico University of Rome, an interdisciplinary programme combining a Master's degree in Medicine and Surgery with a Bachelor's degree in Biomedical Engineering. I previously studied at the Medtec School of Humanitas University and Politecnico di Milano, where I attended the Mathematics course taught by Professor Monica Conti, on which the first part of this compendium is based. Working across these two worlds taught me that the hardest part of entering theoretical machine learning and computational neuroscience is rarely the ideas. It is the mathematical prerequisites that the ideas silently assume.

Books like Bishop's *Pattern Recognition and Machine Learning*, Dayan & Abbott's *Theoretical Neuroscience*, and Sutton & Barto's *Reinforcement Learning* are wonderful, but they move quickly through measure, operators, distributions, stochastic calculus, and variational arguments. Engineering curricula often stop short of these topics, and medical curricula almost never reach them.

This compendium is my attempt to close that gap in a single, coherent, notation-consistent document. It is written for:

- **Engineering, medicine, and computer science students** who want to move into theoretical ML and computational neuroscience without a full mathematics degree.
- **Self-learners** looking for a structured path from first principles to research-level tools.
- **Anyone preparing for graduate study** in theoretical neuroscience, probabilistic machine learning, or computational psychiatry. 

## Contents

| # | Chapter | Main topics |
|---|---------|-------------|
| 1 | **Real and Complex Numbers: Foundations of Analysis** | Field, order and completeness; suprema and infima; decimal expansions and geometric series; countability and Cantor's diagonal argument; complex numbers, polar form, Euler's formula |
| 2 | **Convergence Theory and Numerical Series** | Sequences and limits; monotone convergence and *e*; asymptotic comparison; series, Basel series; convergence tests; absolute and alternating convergence |
| 3 | **Topology of the Real Line, Limits, and Continuity** | Elementary functions; neighbourhoods and the universal definition of limit; notable limits; continuity; extreme and intermediate value theorems |
| 4 | **Differential Calculus and Taylor Approximations** | Derivatives and differentiability; Fermat, Rolle, Lagrange; L'Hôpital; concavity; Taylor's theorem and remainder formulas |
| 5 | **Integral Calculus** | Riemann integral; Fundamental Theorem of Calculus; substitution, parts, partial fractions; improper integrals and their link to probability |
| 6 | **Applied Linear Algebra** | Linear systems; determinants, inverses, rank; vector spaces and fundamental subspaces; linear maps; eigen-decomposition, SVD, least squares, pseudoinverse |
| 7 | **Multivariable Calculus, Vector Operators, and Tensors** | Partial derivatives; gradient, divergence, curl; Hessians and quadratic forms; normal equations; Jacobians; tensors and Einstein notation |
| 8 | **Integral Calculus in Multidimensional Spaces** | Double and triple integrals; change of variables; cylindrical and spherical coordinates; balls in arbitrary dimension; divergence, Green's and Stokes' theorems |
| 9 | **Mathematical Optimization and Convex Programming** | Lagrange multipliers; KKT conditions; convexity and Lagrangian duality; calculus of variations and the Euler–Lagrange equation |
| 10 | **Functional, Fourier, and Complex Analysis** | Hilbert spaces and *L²*; Hilbert–Schmidt operators and the spectral theorem; Sobolev spaces; distribution theory; Fourier transforms; holomorphic functions and residues |
| 11 | **Differential Equations and Dynamical Systems** | First- and second-order ODEs; existence, uniqueness, maximal solutions; stability and local dynamics; solution methods for PDEs |
| 12 | **Probabilistic Foundations and Limit Theorems** | Probability and moment bounds; laws of large numbers and CLT; stochastic differential equations; diffusion equations and stationary probability flows |
| | **References and Recommended Reading** | |

## How to use this compendium

**Please do not read it cover to cover.** It is a reference and a workshop, not a novel.

1. **Start from a target, not from page 1.** Pick the book or paper you want to understand (say, the Gaussian process chapters of PRML, or the Fokker–Planck material in Dayan & Abbott) and work backwards through the chapters it depends on.
2. **Use it as a reference.** The table of contents is detailed down to the subsection so you can jump straight to the tool you need.
3. **Do the derivations by hand.** Read a statement, close the PDF, and try to prove it. Then compare. Mathematical fluency comes from pencil and paper, not from recognition.
4. **Skip what you already know.** Chapters 1–5 are a full analysis course; if you have one behind you, begin at Chapter 6 or 9.
5. **Follow the bridges.** Where a result matters for ML or neuroscience (least squares, KKT, convolution operators, the CLT, diffusion equations), the text says so.
6. **Report what breaks.** If a step is unclear or a proof is wrong, please [open an issue](../../issues). That is the most valuable contribution you can make.

## Repository structure

```text
.
├── README.md
├── LICENSE
├── CITATION.cff
├── CONTRIBUTING.md
├── pdf/
│   └── mathematical-methods-for-ml.pdf   # latest published version
├── src/
│   ├── main.tex
│   ├── chapters/                          # chapter source files
│   ├── figures/                           # TikZ figures
│   └── references.tex                     # recommended reading
└── .github/                               # CI and issue templates
```

## Building from source

Requires a recent TeX distribution (TeX Live or MiKTeX), including TikZ,
PGFPlots, CircuiTikZ, and `latexmk`.

```bash
cd src
latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex
```

The compiled output is `src/main.pdf`. From the repository root, `make build`
runs the same build and `make publish` refreshes the PDF in `pdf/`.

## Status and versioning

This is a **living document**. The first version dates from June 2023 and the current edition was updated in September 2026. Errata and improvements are tracked through [GitHub Issues](../../issues) and [Releases](../../releases).

## Citation

If you use this compendium in your study or research, please cite it. GitHub's **"Cite this repository"** button reads [`CITATION.cff`](CITATION.cff) and produces BibTeX and APA entries.

## Acknowledgments

This work would not exist without **Professor Monica Conti** and the **Politecnico di Milano**. The Analysis course she teaches provided the original foundations on which the first chapters are built, in particular the structure and rigor of the treatment of real analysis, sequences and series, limits, differential and integral calculus, and differential equations.

Everything beyond those foundations, and every error in the text, is my own responsibility. This is an independent, student-authored project and is **not** an official publication of, or endorsed by, Politecnico di Milano.

I am also grateful to the authors of the textbooks that motivated this compendium and to which it is meant as a companion: Christopher Bishop, Peter Dayan and Larry Abbott, and Richard Sutton and Andrew Barto.

## License

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/) (CC BY-NC-SA 4.0). You are free to share and adapt it for non-commercial purposes, provided you give appropriate credit and distribute your contributions under the same license. See [`LICENSE`](LICENSE) for details.

## Author

**Tommaso Vescio**: Medicine and Surgery Medtech student.
Interests: theoretical neuroscience, probabilistic machine learning, computational psychiatry.

*If this helped you, a ⭐ on the repository helps others find it.*
