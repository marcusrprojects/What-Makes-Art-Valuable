# What Makes Art Valuable: Data Scraping and Analysis of Auction Data

[![Language](https://img.shields.io/badge/Language-Python-blue.svg)](https://www.python.org/)
[![pandas](https://img.shields.io/badge/-Pandas-150458?style=flat-square&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Selenium](https://img.shields.io/badge/-Selenium-43B02A?style=flat-square&logo=selenium&logoColor=white)](https://www.selenium.dev/)

## Project Overview

This project explores factors influencing artwork prices at major auction houses (Christie's and Sotheby's). Using custom web scrapers built with Python and Selenium, auction data was collected, including artwork details, estimates, and final sale prices. The data was then cleaned and processed using Pandas to analyze trends, particularly the relationship between auction house estimates, artist popularity (approximated via Yahoo search results), and final sale prices.

## Key Features

*   **Multi-Stage Web Scraping:** Python scripts utilizing Selenium to navigate dynamic auction sites, collect auction/artwork URLs, and extract specific artwork features (price, artist, estimates, dimensions, etc.).
*   **Data Cleaning & Processing:** Jupyter Notebooks demonstrating data cleaning techniques with Pandas, including:
    *   Handling inconsistencies in scraped data.
    *   Parsing and separating estimate ranges (low/high).
    *   Standardizing and converting currencies (GBP, EUR, HKD, etc.) to USD.
    *   Filtering out non-painting/print lots.
*   **Feature Engineering:**
    *   Calculation of artist age and determination of living status.
    *   Creation of binary 'Sold' status based on price data.
    *   Calculation of estimate accuracy (whether the final price fell below, within, or above the estimate range).
    *   Integration of artist popularity metric derived from scraping Yahoo search result counts using Requests and BeautifulSoup.
*   **Exploratory Data Analysis (EDA):** Initial visualizations exploring the relationship between sale prices, estimates (confirming underestimation bias and anchoring effects), and artist popularity.
*   *(Experimental)* An included notebook explores image classification using Keras/TensorFlow (VGG16), though this feature was not integrated into the final analysis.

## Key Technologies

*   **Python:** Core programming language.
*   **Selenium:** Web browser automation and scraping dynamic websites.
*   **Pandas:** Data manipulation, cleaning, and analysis.
*   **NumPy:** Numerical operations.
*   **Requests & BeautifulSoup:** Scraping static content (used for Yahoo search results).
*   **Jupyter Notebook:** Development environment for scraping, cleaning, and analysis.
*   **Matplotlib & Seaborn:** Data visualization.
*   **(Experimental):** Keras / TensorFlow

## Key Findings

*   A strong correlation was observed between auction house estimates (both low and high) and the final sale price, suggesting a potential anchoring bias effect.
*   The analysis indicated a tendency for the auction house (Christie's data was primarily used for this part) to underestimate artwork values, with a significant percentage (~54%) selling above the high estimate.
*   Artist popularity, as approximated by Yahoo search result counts, did not show a strong correlation with final sale prices within this dataset.

## Challenges

*   **Data Collection:** Navigating the complexities of Selenium for dynamic websites and handling inconsistencies across different auction/artwork page layouts.
*   **Data Cleaning:** Significant effort was required to standardize formats, currencies, and filter out irrelevant lots (e.g., furniture).
*   **Scope:** Difficulty in reliably filtering *only* paintings/prints and excluding medium as a feature might introduce noise into the analysis (e.g., comparing a Picasso print to a painting).

## Usage Note

The web scrapers were developed based on the website structures of Christie's and Sotheby's at the time of the project's creation. Websites change frequently, so these scrapers **will likely require significant updates** to function correctly now. The cleaned data files (`.csv`) are provided for direct analysis.

## Project Files

### Data Collection and Cleaning
- [Stage1_Christies_Scraper.ipynb](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/Christies%20web%20scraper/Stage1_Christies_Scraper.ipynb): Data collection and initial scraping.
- [Stage2-Christies_Scraper.ipynb](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/Christies%20web%20scraper/Stage2-Christies_Scraper.ipynb): Further data collection and scraping.
- [Christies_Art_Objects_Clean.csv](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/Clean%20Data/Christies_Art_Objects_Clean.csv): Cleaned data from Christie's.
- [Christies_data with popularity.csv](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/Clean%20Data/Christies_data%20with%20popularity.csv): Data from Christie's with artist popularity measures.
- [SothebysData_clean.csv](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/Clean%20Data/SothebysData_clean.csv): Cleaned data from Sotheby's.

### Data Processing and Visualization
- [Art_Object_Info2.csv](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/Clean%20Data/Art_Object_Info2.csv): Processed data with added features.
- [SothebysData.csv](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/Raw%20Data/SothebysData.csv): Data from Sotheby's.
- [Sotheby's Scraper .ipynb](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/Sotheby's%20Scraper/Sotheby's%20Scraper%20.ipynb): Scraping data from Sotheby's.
- [Art_Object_URL.csv](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/Sotheby's%20Scraper/Art_Object_URL.csv): URLs for art objects.
- [Christies Data Visualization.ipynb](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/Christies%20Data%20Visualization.ipynb): Visualizations of Christie's data.
- [Christies_Art Data Cleaner.ipynb](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/Christies%20Data%20Visualization.ipynb): Data cleaning for Christie's data.
- [Christies_Art Data Cleaner_With Day, Month, Year.ipynb](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/Christies%20Data%20Visualization.ipynb): Detailed data cleaning for Christie's data.
- [Data Cleaner_Christies.ipynb](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/Christies%20Data%20Visualization.ipynb): Data cleaning and processing for Christie's data.
- [Data Visualization_Christies.ipynb](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/Christies%20Data%20Visualization.ipynb): Further data visualization for Christie's data.
- [ImageClassifier.ipynb](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/ImageClassifier.ipynb): Image classification experiments.
- [Sothebys_Data_Cleaner.ipynb](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/Sothebys_Data_Cleaner.ipynb): Data cleaning for Sotheby's data.
- [What Makes Art Valuable_ Data Scraping and Exploratory Data Visualizations.pdf](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/What%20Makes%20Art%20Valuable_%20Data%20Scraping%20and%20Exploratory%20Data%20Visualizations.pdf): The blog post about the project.
- [relative popularity.ipynb](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/relative%20popularity.ipynb): Notebook for analyzing artist popularity.

## Further Reading

For a more detailed discussion of the methodology, findings, and visualizations, please see the [project blog post PDF](What%20Makes%20Art%20Valuable_%20Data%20Scraping%20and%20Exploratory%20Data%20Visualizations.pdf).
