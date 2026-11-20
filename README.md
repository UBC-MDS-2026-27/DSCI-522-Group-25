------------------------------------------------------------------------

editor_options: markdown: wrap: sentence ---

# DSCI-522-Group-25

## Predicting Billboard Top 100 top 10 Songs Using Audio Features and Metadata

Authors: Nitpreet Bamra, Eshadhi Bogoda, Jack Liu, James Wang This project was developed by Team 25 as part of DSCI 522: Data Science Workflows in the University of British Columbia's MDS program (2026–2027).

## Project Overview/Summary

What makes a song reach the top of the Billboard charts? While music success is influenced by various factors, characteristics such as a song's audio features, genre, and release era may help explain differences in chart performance.

Our project investigates whether these characteristics can predict if a song appearing on the Billboard Hot 100 will reach the Top 10. Using historical Billboard chart data and song-level audio information from public datasets on Kaggle, we explore relationships between musical characteristics and chart success and develop a machine learning classification model to identify patterns associated with Top 10 songs.

Our primary research question is: **Can a song's audio features, genre, and release era predict whether a Billboard Hot 100 song reaches the Top 10?**

The results of this analysis may provide insight into which musical characteristics are associated with higher chart positions and how effectively these features can predict Top 10 performance. However, chart success is also influenced by factors such as marketing, audience preferences, and social media trends, which may not be captured in the available data.

Findings/Model results:....


### Dataset

Our project uses the Billboard Hot 100 Audio Features public dataset, published on Kaggle, which can be found at <https://www.kaggle.com/datasets/thedevastator/billboard-hot-100-audio-features>

Our analysis combines two files from this dataset:

Hot Stuff.csv: Contains historical Billboard Hot 100 chart information, including song titles, performers, and chart performance. Hot 100 Audio Features.csv: Contains audio characteristics and metadata associated with songs appearing on the Billboard Hot 100.

The two files are merged using song titles and performers as matching identifiers. The combined dataset is then processed to investigate whether audio features, genre, and release era can predict Top 10 chart performance. The response variable is a binary indicator representing whether a song reached the Billboard Hot 100 Top 10.

The data is downloaded programmatically using the Python kagglehub package. Original data files are stored in data/raw/, while cleaned and processed data is stored in data/processed/.

Dataset Source: [Billboard Hot 100 Audio Features](https://www.kaggle.com/datasets/thedevastator/billboard-hot-100-audio-features), published by `thedevastator` on Kaggle. Dataset license: Data files © Original Authors

### Running the Analysis

The following instructions describe how to reproduce the analysis locally.

1.  Prerequisites

Ensure that the following software is installed:

Git — for cloning the repository.

Python — for running the analysis.

uv — for managing the Python environment and dependencies.

Quarto — for rendering the analysis report.

2.  Clone the Repository

Open a terminal in git bash and run:

``` bash
git clone <https://github.com/UBC-MDS-2026-27/DSCI-522-predicting-top-10-billboard-hits-using-audio-features-and-metadata.git>

cd DSCI-522-predicting-top-10-billboard-hits-using-audio-features-and-metadata
```

3.  Set Up the Environment

Install the required Python packages using:

``` bash
uv sync
```

4.  Download the Dataset

The analysis uses kagglehub to download the dataset directly from Kaggle.

The dataset is identified by:
```bash
dataset = "thedevastator/billboard-hot-100-audio-features"
```
The following files are downloaded:

Hot Stuff.csv Hot 100 Audio Features.csv

The download process is included in the analysis code, so the data does not need to be downloaded manually. But before running the report, create the data folders if they do not already exist by running:

``` bash
mkdir -p data/raw data/processed
```

5.  Run the Analysis

From the root directory of the repository, run:

``` bash
cd analysis 
uv run quarto render analysis/report.qmd
```

Run the render command inside analysis/

The analysis performs data loading, cleaning, exploratory data analysis, model training, and evaluation. The results are presented in a rendered HTML report.

6.  View the Report

After rendering, open the generated HTML file in the analysis/ directory.

The report is also available online at : ........

### Dependencies

This project uses Python(3.14 or later) for data processing, visualization, and machine learning. The main libraries include:

- pandas and numpy for data manipulation and numerical operations.

- kagglehub for downloading the dataset.

- scikit-learn for preprocessing, classification, and model evaluation.

- Quarto is used to generate the final analysis report.

- Python package dependencies and their versions are managed using uv. For the complete list of dependencies, refer to pyproject.toml and uv.lock.

### License

The following licenses are proposed for this project:

Code: MIT License

Report: Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)

For the complete license terms, see LICENSE.md.

The original Kaggle dataset is subject to its own licensing terms.

### Generative AI Usage

Generative AI tools were used to assist with various aspects of the project's documentation and code development.

ChatGPT (OpenAI) was used to help draft and organize project documentation, including the README.

Claude (Anthropic) was used to assist with reviewing and designing portions of the data download code.
