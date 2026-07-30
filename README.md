# MFRE Coding Workshop 2026

Material for the 2026 coding bootcamp in the Master of Food and Resource
Economics (MFRE) program at the University of British Columbia. The workshop
introduces Python and R for data import, cleaning, visualization, statistical
testing, and introductory modeling.

Repository: `https://github.com/UBC-MFRE/python-r-workshop-2026`

## Before The Bootcamp

Incoming students complete the Python and R preparation package before the
August bootcamp:

[UBC-MFRE/Welcome_Package_Summer2026](https://github.com/UBC-MFRE/Welcome_Package_Summer2026)

That companion repository is the self-paced preparation package. This
repository contains the bootcamp material itself and assumes students have
already worked through the preparation package.

## Setup

### Python

Install the [Anaconda Distribution](https://www.anaconda.com/download). It
includes Python, JupyterLab, and the main scientific computing libraries used in
the notebooks.

For a reproducible package set, create or activate your workshop environment and
install the tested dependencies:

```bash
pip install -r requirements.txt
```

The tested package set pins the libraries used in the current notebooks. In
particular, use `statsmodels>=0.14.5`; `statsmodels==0.14.4` is incompatible
with `scipy==1.16.x`.

### R

Install [R](https://cran.r-project.org/) first, then
[RStudio Desktop](https://posit.co/download/rstudio-desktop/). Open the
relevant `.Rproj` file before opening an `.Rmd` file so that project-relative
paths resolve correctly.

Install the R packages used by the workshop:

```r
install.packages(c(
  "pacman", "tidyverse", "tidyr", "tibble", "dplyr", "ggplot2",
  "readr", "here", "knitr", "rmarkdown", "broom", "lmtest",
  "sandwich", "janitor", "scales", "forecast", "zoo", "class",
  "skimr"
))
```

### Data

Clone the repository to get the notebooks, R Markdown files, and datasets:

```bash
git clone https://github.com/UBC-MFRE/python-r-workshop-2026.git
cd python-r-workshop-2026
```

Shared datasets are in [data/](data/). The Day 5 policy dataset is in
[stat applications/r_applications/policy_analysis.csv](stat%20applications/r_applications/policy_analysis.csv)
and is used by both the Python and R statistics applications.

Keep the folder layout intact. Several notebooks use paths such as
`../../../data/gapminder.csv`, which are relative to the notebook location.

## Schedule

Dates, room, and exact times for 2026 are TBC. The day and session structure is
below.

| Day | Morning session | Afternoon session |
| --- | --- | --- |
| Day 1 (Mon, TBC) | Intro to Python (I) | Hands-on coding (I) |
| Day 2 (Tue, TBC) | Intro to Python (II) | Hands-on coding (II) |
| Day 3 (Wed, TBC) | Intro to R (I) | Hands-on coding (I) |
| Day 4 (Thu, TBC) | Intro to R (II) | Hands-on coding (II) |
| Day 5 (Fri, TBC) | Stat applications in Python: summary statistics and hypothesis tests | Stat applications in R: summary statistics and hypothesis tests |

## Python Material

Python runs on the first two workshop days. Folder names below are Python day
numbers, not calendar dates.

### Python Day 1

Part 1:

- [1_Jupyter_and_Python.ipynb](python/Day%201/Part-1/1_Jupyter_and_Python.ipynb) - JupyterLab, Python syntax, variables, and the interactive workflow.
- [2_Data_Types_and_Structures.ipynb](python/Day%201/Part-1/2_Data_Types_and_Structures.ipynb) - data types, lists, dictionaries, and indexing.

Part 2:

- [4_Functions_and_Conditionals.ipynb](python/Day%201/Part-2/4_Functions_and_Conditionals.ipynb) - functions, arguments, conditionals, and pandas conditions.
- [5_Iteration_and_Visualization.ipynb](python/Day%201/Part-2/5_Iteration_and_Visualization.ipynb) - loops, vectorization, pandas methods, and first plots.

### Python Day 2

- [1_Intro_to_Data_Science.ipynb](python/Day%202/Part-1/1_Intro_to_Data_Science.ipynb) - data import, cleaning, and exploratory analysis with greenhouse gas emissions data.
- [2_Intro_to_Modeling.ipynb](python/Day%202/Part-2/2_Intro_to_Modeling.ipynb) - regression, classification, and model evaluation.

### Day 5 Python

- [python_applications.ipynb](stat%20applications/python_applications/python_applications.ipynb) - hypothesis tests, group comparisons, and regression with the climate policy dataset.

## R Material

### Day 3 R

- [1_Intro_to_R.Rmd](r/Day%201/1_Intro_to_R.Rmd) - R data structures, control flow, functions, and coding style. Open [r/r.Rproj](r/r.Rproj) first.
- [1_Intro_to_R.nb.html](r/Day%201/1_Intro_to_R.nb.html) - rendered notebook for reading.

### Day 4 R

- [2_Intro_to_Modeling_R.Rmd](r/Day%202/2_Intro_to_Modeling_R.Rmd) - `dplyr`, `ggplot2`, and applied data cleaning.
- [2_Intro_to_Modeling_R.nb.html](r/Day%202/2_Intro_to_Modeling_R.nb.html) - rendered notebook for reading.

### Day 5 R

- [r_applications.Rmd](stat%20applications/r_applications/r_applications.Rmd) - the hypothesis-testing workflow in R. Open [r_applications.Rproj](stat%20applications/r_applications/r_applications.Rproj) first.

## Background Reading

- [climate change pledges actions and outcomes.pdf](resources/climate%20change%20pledges%20actions%20and%20outcomes.pdf) - source paper behind the climate policy dataset used on Day 5.

## Repository Structure

```text
python-r-workshop-2026/
    README.md
    LICENSE
    requirements.txt
    data/
        2014wesp_country_classification.pdf
        age.csv
        blood_type.csv
        food_cpi.csv
        gapminder.csv
        gapminder_gni.csv
        pollution.csv
        pollution_missing.csv
        province_names.csv
        province_weather.csv
        province_weather_fahrenheit.csv
        random.csv
        regional_emissions.csv
        sector_emissions.csv
        temp.csv
        temperature.csv
        chis_data/
            chis_eng.csv
            chis_esp.csv
            chis_other.csv
    img/
        Python-data-structure.jpeg
        filetree.png
        for.png
        functions.png
        gap_ex.png
        list-index.png
        sepal.png
        vectorized.png
        vectorized2.png
    python/
        Day 1/
            Part-1/
                1_Jupyter_and_Python.ipynb
                2_Data_Types_and_Structures.ipynb
            Part-2/
                4_Functions_and_Conditionals.ipynb
                5_Iteration_and_Visualization.ipynb
        Day 2/
            Part-1/
                1_Intro_to_Data_Science.ipynb
                regional_emissions.csv
                sector_emissions.csv
            Part-2/
                2_Intro_to_Modeling.ipynb
    r/
        r.Rproj
        Day 1/
            1_Intro_to_R.Rmd
            1_Intro_to_R.nb.html
        Day 2/
            2_Intro_to_Modeling_R.Rmd
            2_Intro_to_Modeling_R.nb.html
    resources/
        climate change pledges actions and outcomes.pdf
    stat applications/
        python_applications/
            python_applications.ipynb
        r_applications/
            policy_analysis.csv
            r_applications.Rmd
            r_applications.Rproj
    Previous Years/
```

## Notes

- The Day 1 Python folder contains notebooks numbered `1`, `2`, `4`, and `5`;
  there is no separate current-year notebook numbered `3`.
- The copies of `regional_emissions.csv` and `sector_emissions.csv` in
  `python/Day 2/Part-1/` match the copies in `data/`.
- `Previous Years/` contains archived material and is not part of the 2026
  workshop execution path.

## License

See [LICENSE](LICENSE).
