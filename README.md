# WEIRD FAccTs: How Western, Educated, Industrialized, Rich, and Democratic is FAccT?

Authors: Ali Akbar Septiandri, Marios Constantinides, Mohammad Tahaei, Daniele Quercia

Nokia Bell Labs, Cambridge, United Kingdom

To appear at ACM FAccT 2023

## Abstract

Studies conducted on **W**estern, **E**ducated, **I**ndustrialized, **R**ich, and **D**emocratic (WEIRD) samples are considered atypical of the world's population and may not accurately represent human behavior. In this study, we aim to quantify the extent to which the ACM FAccT conference, the leading venue in exploring Artificial Intelligence (AI) systems' fairness, accountability, and transparency, relies on WEIRD samples. We collected and analyzed 128 papers published between 2018 and 2022, accounting for 30.8% of the overall proceedings published at FAccT in those years (excluding abstracts, tutorials, and papers without human-subject studies or clear country attribution for the participants). We found that 84% of the analyzed papers were exclusively based on participants from Western countries, particularly exclusively from the U.S. (63%). Only researchers who undertook the effort to collect data about local participants through interviews or surveys added diversity to an otherwise U.S.-centric view of science. Therefore, we suggest that researchers collect data from under-represented populations to obtain an inclusive worldview. To achieve this goal, scientific communities should champion data collection from such populations and enforce transparent reporting of data biases.

## Installation

Clone the repository to your local machine using Git:

```bash
git clone https://github.com/aliakbars/weird-facct.git
```

Install Poetry, a dependency manager for Python:
```bash
curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python -
```

Alternatively, you can install Poetry using pip:
```bash
pip install poetry
```

Navigate to the project directory and use Poetry to install the required dependencies:
```bash
poetry install
```

## Usage

To reproduce the results and images in the paper, run the `facct.ipynb` file.

## Datasets

Files named using the `chi*` pattern have been extracted from the supplementary materials available [here](https://dl.acm.org/doi/10.1145/3411764.3445488).
Files related to FAccT have been manually extracted or gathered from metadata. Datasets necessary for metric calculations are also provided, as detailed in the table below:

| Symbol | Variable       | Formula                                    | Description        | File          |
|--------|----------------|--------------------------------------------|--------------------|---------------|
| $W_c$  | Western        | $1 \text{ if } c \in \text{ Western else } 0$ | Whether country $c$ is Western based on Huntington classification (Huntington, 2000) | `western.csv` |
| $E_c$  | Educated       | $\mathbb{E}_c[\text{years of schooling}]$ | Mean years of schooling for country $c$ based on UNDP Human Development Report (2022) | `edu.csv` |
| $I_c$  | Industrialized | $\text{GDP per capita}_c$ | Level of industrialization for country $c$ based on World Bank GDP per capita, PPP (current Int\$, 2020) | `gdp.csv` |
| $R_c$  | Rich           | $\text{GNI per capita}_c$ | Wealth of country $c$ based on World Bank GNI per capita, PPP (current Int\$, 2020) | `gni.csv` |
| $D_c$  | Democratic     | $\text{political rights}_c$ | Level of democracy for country $c$ based on Freedom House Political Rights (2022) | - |
