# ProcessLayout: Multi-Objective MINLP Optimization for Multi-Floor Process Layout

[![DOI](https://img.shields.io/badge/DOI-10.1016%2Fj.cie.2025.111442-blue)](https://doi.org/10.1016/j.cie.2025.111442)
[![Journal](https://img.shields.io/badge/Journal-Computers%20%26%20Industrial%20Engineering-orange)](https://www.sciencedirect.com/journal/computers-and-industrial-engineering)
[![License](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
[![GAMS](https://img.shields.io/badge/Code-GAMS-red)](https://www.gams.com/)
[![Aspen Plus](https://img.shields.io/badge/Simulation-Aspen%20Plus-purple)](https://www.aspentech.com/)

## About

This repository contains the GAMS optimization code, Aspen Plus simulation files, and demonstration videos accompanying the paper on **integrated multi-objective Mixed-Integer Nonlinear Programming (MINLP) optimization** for **cost-effectiveness and safety** in **multi-floor process layout design** for manufacturing industries. The framework is demonstrated through five industrial case studies covering biodiesel, ethylene glycol, polyacrylate, potassium chloride, and urea production plants.

## Associated Publication

> **Sukpancharoen, S., Udol, P., Supsomboon, P., & Srinophakun, T. R.** (2025). Integrated multi-objective MINLP optimization for cost-effectiveness and safety in multi-floor process layout for manufacturing industries. *Computers & Industrial Engineering*, *209*, 111442. https://doi.org/10.1016/j.cie.2025.111442

📄 Available at [ScienceDirect](https://doi.org/10.1016/j.cie.2025.111442).

## Key Features

- **Multi-objective MINLP formulation** balancing capital cost, operating cost, and safety risk.
- **Multi-floor layout design** that simultaneously determines equipment placement, floor assignment, and safety distances.
- **Five real-world case studies** spanning diverse chemical and process industries.
- Reproducible workflow combining **GAMS** (optimization) with **Aspen Plus** (process simulation).
- **Video demonstrations** illustrating the resulting layouts for each case study.

## Case Studies

The repository provides complete files for five industrial process layouts:

| # | Process | Product | Industry |
|---|---------|---------|----------|
| 1 | **Biodiesel Production** | Biodiesel (FAME) | Renewable energy / Oleochemicals |
| 2 | **Ethylene Glycol Plant** | Ethylene glycol | Petrochemicals / Antifreeze |
| 3 | **Polyacrylate Plant** | Polyacrylate polymer | Specialty polymers |
| 4 | **Potassium Chloride Plant** | KCl (potash) | Fertilizer / Mining |
| 5 | **Urea Plant** | Urea | Fertilizer / Agrochemicals |

## Repository Structure

```
ProcessLayout/
│
├── GAMS Optimization Code (.gms)
│   ├── Biodiesel Code_GAMS.gms
│   ├── Ethylene Code_GAMS.gms
│   ├── Polyacrylate Code_GAMS.gms
│   ├── Potassium Chloride Code_GAMS.gms
│   └── Urea Code_GAMS.gms
│
├── Aspen Plus Simulation Files (.bkp / .apwz)
│   ├── Biodiesel Production.bkp
│   ├── Ethylene Glycol Plant.bkp
│   ├── polyacrylate Plant.bkp
│   ├── Potassium Chloride Plant.bkp
│   └── urea Plant.apwz
│
└── Demonstration Videos (.mp4)
    ├── VDO Biodiesel.mp4
    ├── VDO Ethylene-glycol.mp4
    ├── VDO Polyacrylate.mp4
    ├── VDO Potassium Chloride.mp4
    └── VDO Urea.mp4
```

Each case study consists of a paired set of files: a `.gms` GAMS script that solves the MINLP layout optimization, an Aspen Plus model (`.bkp` or `.apwz`) that supplies the underlying process data, and an `.mp4` video that visualizes the resulting multi-floor layout.

## Software Requirements

| Software | Purpose | Notes |
|----------|---------|-------|
| **GAMS** (≥ 36) | MINLP optimization | Requires a solver capable of MINLP (e.g., DICOPT, BARON, SBB, ANTIGONE) |
| **Aspen Plus** (V12.1 or compatible) | Process simulation | Required to open `.bkp` / `.apwz` files |
| **Video player** | View `.mp4` demos | Any standard player (VLC, Windows Media Player, QuickTime) |

## Usage

### Download

```bash
git clone https://github.com/sombsuk/ProcessLayout.git
cd ProcessLayout
```

Or download individual files directly from the GitHub web interface.

### Running a Case Study

For each case study, the recommended workflow is:

1. Open the corresponding Aspen Plus file (`.bkp` / `.apwz`) to inspect the process flowsheet, equipment list, and unit dimensions used as inputs.
2. Open the matching GAMS file (`.gms`) and configure the solver options as needed.
3. Solve the MINLP problem in GAMS to obtain the optimized multi-floor layout.
4. Refer to the demonstration video (`VDO *.mp4`) to visualize the optimized layout.

For full methodological details — including the mathematical formulation, objective functions, constraints, safety considerations, and parameter values — please refer to the [associated publication](https://doi.org/10.1016/j.cie.2025.111442).

## Citation

If you use the code or simulation files in this repository, please cite:

**BibTeX:**
```bibtex
@article{Sukpancharoen2025layout,
  title   = {Integrated multi-objective MINLP optimization for cost-effectiveness and safety in multi-floor process layout for manufacturing industries},
  author  = {Sukpancharoen, Somboon and Udol, Prawdown and Supsomboon, Pornpitcha and Srinophakun, Thongchai Rohitatisha},
  journal = {Computers \& Industrial Engineering},
  volume  = {209},
  pages   = {111442},
  year    = {2025},
  doi     = {10.1016/j.cie.2025.111442},
  url     = {https://doi.org/10.1016/j.cie.2025.111442}
}
```

## Authors and Affiliations

| Author | Role | Affiliation |
|--------|------|-------------|
| **Somboon Sukpancharoen** | First author | Department of Agricultural Engineering, Faculty of Engineering, Khon Kaen University, Thailand |
| Prawdown Udol | Co-author | Department of Agricultural Engineering, Faculty of Engineering, Khon Kaen University, Thailand |
| Pornpitcha Supsomboon | Co-author | Department of Chemical Engineering, Faculty of Engineering, Kasetsart University, Thailand |
| **Thongchai Rohitatisha Srinophakun** | **Corresponding author** | Department of Chemical Engineering, Faculty of Engineering, Kasetsart University, Thailand |

## License

This repository is released under the **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)** license. This means you may:

- ✅ **Share** — copy and redistribute the material in any medium or format
- ✅ **Attribute** — give appropriate credit to the authors and cite the publication

But you may **not**:

- ❌ **NonCommercial** — use the material for commercial purposes without permission
- ❌ **NoDerivatives** — distribute modified versions of the material

For full license terms, see [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/).

The associated publication remains subject to the publisher's copyright. When using or adapting these materials, please cite the publication and respect the publisher's terms.

## Contact

**For questions about the publication:**
Prof. Thongchai Rohitatisha Srinophakun *(Corresponding Author)*
Department of Chemical Engineering, Faculty of Engineering
Kasetsart University, Bangkok 10900, Thailand

**For questions about this repository:**
Assoc. Prof. Somboon Sukpancharoen, Ph.D. *(Repository Maintainer)*
Department of Agricultural Engineering, Faculty of Engineering
Khon Kaen University, Khon Kaen 40002, Thailand
📧 sombsuk@kku.ac.th
