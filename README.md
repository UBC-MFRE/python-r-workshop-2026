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

Shared datasets are in [data/](data/). The statistics applications policy dataset is in
[stat applications/r_applications/policy_analysis.csv](stat%20applications/r_applications/policy_analysis.csv)
and is used by both the Python and R statistics applications.

Keep the folder layout intact. Several notebooks use paths such as
`../../../data/gapminder.csv`, which are relative to the notebook location.

## Schedule

All dates are 2026 and follow the MFRE 2026-2027 program schedule. Python runs
in the August Data Analytics week. R runs in Term 1 alongside FRE 528.

Rooms: MCLD 2018 is the MacLeod building; MCML 154 is MacMillan; ORCH 4018 is
Orchard Commons.

### Python

| Date | Session | Time | Room |
| --- | --- | --- | --- |
| Wed 19 Aug | Intro to Python (I) | 9:30 to 12:30 | MCLD 2018 |
| Wed 19 Aug | Intro to Python (I), hands-on coding | 1:30 to 3:30 | MCLD 2018 |
| Thu 20 Aug | Intro to Python (II) | 9:30 to 12:30 | MCLD 2018 |
| Thu 20 Aug | Intro to Python (II), hands-on coding | 1:30 to 3:30 | MCLD 2018 |
| Fri 21 Aug | Stat applications in Python | 9:30 to 11:30 | MCLD 2018 |

Total Python contact time is 12 hours.

### R

| Date | Session | Time | Room |
| --- | --- | --- | --- |
| Fri 11 Sep | Intro to R (I) | 12:00 to 2:00 | MCML 154 |
| Fri 11 Sep | Intro to R (II) | 3:00 to 5:00 | MCML 154 |
| Wed 16 Sep | Intro to R (I and II), hands-on coding | 3:00 to 5:00 | ORCH 4018 |
| Fri 18 Sep | Stat applications in R | 12:00 to 2:00 | ORCH 4018 |

Total R contact time is 8 hours.

The schedule grid gives no stated end time for Intro to R (I). The 2:00 end
above is read from the extent of the block in the grid, matching the layout
used for the other sessions. Confirm before preparing that session.

## Python Material

Python runs on Wed 19 and Thu 20 August. Folder names below are Python session
numbers, not calendar dates.

### Intro to Python (I), Wed 19 Aug

Part 1:

- [1_Jupyter_and_Python.ipynb](python/Day%201/Part-1/1_Jupyter_and_Python.ipynb) - JupyterLab, Python syntax, variables, and the interactive workflow.
- [2_Data_Types_and_Structures.ipynb](python/Day%201/Part-1/2_Data_Types_and_Structures.ipynb) - data types, lists, dictionaries, and indexing.

Part 2:

- [4_Functions_and_Conditionals.ipynb](python/Day%201/Part-2/4_Functions_and_Conditionals.ipynb) - functions, arguments, conditionals, and pandas conditions.
- [5_Iteration_and_Visualization.ipynb](python/Day%201/Part-2/5_Iteration_and_Visualization.ipynb) - `for` loops, iteration over lists and strings, pandas methods, and first plots.

### Intro to Python (II), Thu 20 Aug

- [1_Intro_to_Data_Science.ipynb](python/Day%202/Part-1/1_Intro_to_Data_Science.ipynb) - data import, cleaning, and exploratory analysis with greenhouse gas emissions data.
- [2_Intro_to_Modeling.ipynb](python/Day%202/Part-2/2_Intro_to_Modeling.ipynb) - regression, classification, and model evaluation.

### Stat applications, Python (Fri 21 Aug)

- [python_applications.ipynb](stat%20applications/python_applications/python_applications.ipynb) - hypothesis tests, group comparisons, and regression with the climate policy dataset.

## R Material

### Intro to R (I), Fri 11 Sep

- [1_Intro_to_R.Rmd](r/Day%201/1_Intro_to_R.Rmd) - R data structures, control flow, functions, and coding style. Open [r/r.Rproj](r/r.Rproj) first.
- [1_Intro_to_R.nb.html](r/Day%201/1_Intro_to_R.nb.html) - rendered notebook for reading.

### Intro to R (II), Fri 11 Sep

- [2_Intro_to_Modeling_R.Rmd](r/Day%202/2_Intro_to_Modeling_R.Rmd) - `dplyr`, `ggplot2`, and applied data cleaning.
- [2_Intro_to_Modeling_R.nb.html](r/Day%202/2_Intro_to_Modeling_R.nb.html) - rendered notebook for reading.

### Stat applications, R (Fri 18 Sep)

- [r_applications.Rmd](stat%20applications/r_applications/r_applications.Rmd) - the hypothesis-testing workflow in R. Open [r_applications.Rproj](stat%20applications/r_applications/r_applications.Rproj) first.

## Background Reading

- [climate change pledges actions and outcomes.pdf](resources/climate%20change%20pledges%20actions%20and%20outcomes.pdf) - source paper behind the climate policy dataset used in the statistics applications sessions.

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
