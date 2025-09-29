# Time Series Analysis — Problem Sets and Final Report (A.Y. 2024/2025)

This repository contains the problem sets and final report for the “Time Series Analysis” course (Academic Year 2024/2025). Materials are provided as reproducible Quarto notebooks (.qmd) alongside rendered HTML/PDF outputs and any supporting data or graphics.

Most of the repository’s tracked code is rendered HTML (reports), with some embedded JavaScript from the rendering process.

## Repository structure

```
.
├─ ps1/
│  ├─ Assignment1.qmd                # Quarto source for problem set 1
│  ├─ Assignment1.html               # Rendered HTML for problem set 1
│  ├─ TS_20236_Assignment_1.pdf      # PDF output for problem set 1
│  ├─ gistemp.RData                  # Supporting data (PS1)
│  ├─ gistemp.txt                    # Supporting data (PS1)
│  ├─ 00001a.png                     # Figure asset (PS1)
│  ├─ graph_1.pdf                    # Figure asset (PS1)
│  ├─ Assignment1_files/             # Quarto-generated assets
│  └─ output_ps1/                    # PS1 generated outputs (figures/tables)
├─ ps2/                               # Problem set 2 (materials as added)
├─ ps3/                               # Problem set 3 (materials as added)
├─ ps4/                               # Problem set 4 (materials as added)
├─ ps5/                               # Problem set 5 (materials as added)
├─ fp/                                # Final project/report (materials as added)
├─ LICENSE
└─ README.md
```

Each `psN/` folder corresponds to problem set N and typically includes:
- A Quarto source file (`AssignmentN.qmd` or similarly named)
- A rendered report (`.html` and/or `.pdf`)
- Any supporting data files and generated figures/tables

The `fp/` folder contains the final project/report in the same pattern.

## How to use this repository

- View reports directly:
  - Open the rendered `.html` files (e.g., `ps1/Assignment1.html`) in your web browser.
  - PDFs can be viewed with any PDF reader (e.g., `ps1/TS_20236_Assignment_1.pdf`).

- Reproduce the analyses locally by rendering the Quarto sources.

## Reproducing the analyses

### Prerequisites

- Quarto (recommended)
  - Installation and setup: https://quarto.org/docs/get-started/
- R (for R-based Quarto documents)
  - Download: https://cran.r-project.org/

Optional:
- RStudio (for an IDE workflow with Quarto integration): https://posit.co/download/rstudio-desktop/

Note:
- Each `.qmd` file declares its own code and library requirements. Install any packages referenced at the top of the document (e.g., `install.packages("package-name")`) before rendering.

### Render a notebook

From the repository root:

- Using the Quarto CLI:
  - `quarto render ps1/Assignment1.qmd`

- Using R (without the CLI):
  - Open `ps1/Assignment1.qmd` in RStudio and click “Render”
  - Or run in R:
    ```r
    install.packages("quarto") # if needed
    quarto::quarto_render("ps1/Assignment1.qmd")
    ```

Rendering will create/update the corresponding `.html` (and optionally `.pdf`) outputs and any associated asset folders.

### Data and paths

- Data files required by a problem set are stored within that problem set’s folder (e.g., `ps1/gistemp.RData`, `ps1/gistemp.txt`).
- Relative paths are used where possible; render from the repository root to preserve path structure.

### Reproducibility tips

- If the analysis uses randomness, ensure a seed is set (e.g., `set.seed(...)`) inside the `.qmd` for deterministic runs.
- Record your R and package versions for exact reproducibility (`sessionInfo()`).

## Contributors

- Stefano Graziosi
- Gabriele Molè
- Giovanni Carron
- Laura Lo Schiavo

## License

This project is distributed under the terms specified in [LICENSE](LICENSE). Please review the license before reusing code or content.

Badges:
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
