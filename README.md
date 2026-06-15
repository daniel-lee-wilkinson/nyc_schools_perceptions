# New York City Schools Perception

An R Markdown notebook analysing NYC school survey data to explore how students, teachers, and parents differ in their perceptions of school quality - and whether those perceptions relate to academic outcomes.

## Research Questions

1. Is there a relationship between gender percentages and average SAT scores?
2. Which NYC schools have the best quality metrics according to survey data, and does this differ by respondent type?
3. Do differences in perception between groups (e.g. students vs parents on safety) relate to other variables?

## Data Sources

- **combined.csv** - school-level academic outcomes including average SAT scores and demographic data, loaded directly from a hosted URL
- **masterfile11_gened_final.txt** - survey responses from general education schools
- **masterfile11_d75_final.txt** - survey responses from District 75 (special education) schools

The two survey files must be placed in the project root directory before knitting.

## Survey Metrics

Survey scores (scale 1–10) cover four dimensions, each broken down by respondent type (parent, teacher, student, total):

| Code | Dimension |
|------|-----------|
| `saf` | Safety |
| `com` | Communication |
| `eng` | Engagement |
| `aca` | Academic expectations |

## Key Findings

- Parents consistently rate schools higher than teachers and students across all dimensions
- The largest perception gaps are in **communication** and **safety**
- Students rate lowest, particularly in communication and safety - despite being most directly affected
- Academic expectations show the most consistent scores across groups
- Teachers show wide internal variation in all dimensions

## Requirements

- R 4.0+
- R packages: `tidyverse`, `janitor`, `readr`, `corrplot`

Install all at once:

```r
install.packages(c("tidyverse", "janitor", "readr", "corrplot"))
```

## Setup

1. Clone the repository
2. Place `masterfile11_gened_final.txt` and `masterfile11_d75_final.txt` in the project root
3. Open `notebook.Rmd` in RStudio and knit to HTML or PDF

## Project Structure

```
├── notebook.Rmd                    # Main analysis notebook
├── masterfile11_gened_final.txt    # Survey data - general education schools
├── masterfile11_d75_final.txt      # Survey data - District 75 schools
└── .gitignore
```