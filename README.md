# Game Changers: A Data-Driven Exploration of Team Design and Network Effects in Board Game Innovation

**Author:** Martin Koch  
**Degree Program:** M.Sc. in Computational Social Systems  
**Institution:** RWTH Aachen

- [Full text - PDF Master Thesis](https://github.com/creamartin/master_css/blob/master/CSS_Master_Thesis.pdf)

## Abstract

   >This master's thesis investigates the dynamics of team formation and creative success within the board game industry, utilizing data from BoardGameGeek. By applying the novel Relational Hyper Event Model (RHEM) and Relational Hyper Event Outcome Model (RHOM), we identify key factors influencing collaboration and their impact on creative outcomes. The analysis reveals that prior collaborations and tenure similarity significantly drive team formation, while prior success and diverse mechanical experience correlate with higher creative performance. High-creativity teams are larger, exhibit more skill-related diversity, and have greater mechanical experience. These findings underscore the importance of balancing familiarity and diversity to foster innovation. Methodological insights and future research directions are discussed, highlighting the potential of RHEM and RHOM in practical research contexts.

## Project Overview

This repository contains the data and scripts used for the M.Sc. thesis titled "Game Changers: A Data-Driven Exploration of Team Design and Network Effects in Board Game Innovation." The project explores various aspects of board game innovation, including team design and network effects, using a data-driven approach.

## Directory Structure

   ```
   .
   ├── README.md                  # This file
   ├── bgg_data                   # Data and data preparation
   │   ├── __pycache__            # Compiled Python files
   │   ├── bgg.csv                # Cleaned dataset before eventnet format
   │   ├── bgg_clean.ipynb        # Jupyter notebook for data cleaning/preparation
   │   ├── bgg_explore.ipynb      # Jupyter notebook for visual exploration
   │   ├── bgg_raw                # Raw data from recommend.games
   │   ├── bgg_two_mode_novelty.csv # Eventnet format with novelty as outcome
   │   ├── bgg_two_mode_rating.csv # Eventnet format with rating as outcome
   │   ├── infer_gender           # Procedure for gender inference
   │   └── novelty_computation.py # Procedure to calculate novelty
   ├── eventnet_data              # Eventnet data and configuration
   │   ├── bgg_two_mode_novelty_COND_SIZE_DHE.csv # Computed hyperedge statistics with respect to novelty
   │   ├── bgg_two_mode_rating_COND_SIZE_DHE.csv # Computed hyperedge statistics with respect to rating
   │   ├── config.xml             # Model specification in Eventnet
   │   └── eventnet-1.1.jar       # Java software used for creating observations and statistics
   ├── results                    # Outputs for master thesis
   │   └── {... outputs for master thesis}
   └── scripts                    # R scripts for analysis
      ├── compare_coefficients.R # Script to compare coefficients
      ├── coxph.R                # Script to fit stratified Cox proportional hazards model
      ├── load_data.R            # Script to load data
      ├── ols.R                  # Script to fit Ordinary Least Squares (OLS) model
      ├── results_collinearity.R # Script for collinearity results
      ├── results_correlation.R  # Script for correlation analysis of main variables
      ├── results_h1.R           # Script for hypothesis 1 analysis
      ├── results_h2.R           # Script for hypothesis 2 analysis
      └── results_h3.R           # Script for hypothesis 3 analysis
   ```

## Getting Started

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/creamartin/master_css
   cd <repository-directory>
   ```

2. **Set Up the Environment:**

   - Ensure you have the necessary software installed:
     - Java (for Eventnet software)
     - Python (for Jupyter notebooks and data preparation)
     - R (for statistical analysis)

3. **Python Package Dependencies:**

   Install the required Python packages:

   ```bash
   pip install scikit-learn numpy pandas seaborn matplotlib glob2
   ```

4. **R Package Dependencies:**

   To run the R scripts, install the following R packages:

   ```r
   install.packages(c("dplyr", "knitr", "kableExtra", "survival", "htmltools", "texreg", "car", "stargazer"))
   ```

5. **Data Preparation:**

   - Use `bgg_clean.ipynb` for cleaning and preparing the dataset.
   - Explore the data with `bgg_explore.ipynb`.

6. **Run Analysis:**

   - Perform statistical analyses using the R scripts:
     - `results_correlation.R` for correlation analysis of main variables.
     - `results_h1.R`, `results_h2.R`, and `results_h3.R` for hypothesis analyses.

## Acknowledgements

- **Jürgen Lerner** for feedback on Eventnet ([Eventnet GitHub](https://github.com/juergenlerner/eventnet)).
- **Jana Lasser** for thesis mentoring ([Jana Lasser](https://www.janalasser.at/)).
- **Markus Shepherd** for access to the BGG dataset ([Board Game Geek](https://boardgamegeek.com/)).

## References

- [Eventnet Software Documentation](https://github.com/juergenlerner/eventnet)
- [Board Game Geek Data](https://boardgamegeek.com/)


