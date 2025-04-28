# Christie's Web Scraper Data Science Project

[![Language](https://img.shields.io/badge/Language-Python-blue.svg)](https://www.python.org/)
[![pandas](https://img.shields.io/badge/-Pandas-150458?style=flat-square&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Selenium](https://img.shields.io/badge/-Selenium-43B02A?style=flat-square&logo=selenium&logoColor=white)](https://www.selenium.dev/)

## Project Overview

This data science project aims to investigate the factors influencing the prices of artworks at auction, focusing on the prestige or popularity of artists and the reliability of auction house estimates. The project involves data collection, cleaning, processing, and visualization.

## Data Collection

We gathered data from Sotheby's and Christie's auction websites using web scrapers built with Selenium, a Python library for automating web browsers. The scrapers collected URLs for each auction and artwork, along with key features such as price, artist, and estimate price.

## Data Cleaning

The collected data required substantial cleaning, including separating high and low estimate prices, converting all prices to USD, and standardizing names and formats. We also filtered out unwanted art forms.

## Data Processing

After data cleaning, we added features to gain insights into artwork pricing. Using Pandas DataFrames, BeautifulSoup, requests libraries, and the Yahoo API, we collected the number of Yahoo search results for each artist as a measure of their popularity. We also created new features, such as artist age, artwork status, and the accuracy of auction house estimates.

## Data Visualization

We visualized the data to understand auction house estimate bias and correlations between sale prices and estimates. The project primarily focuses on the data and its analysis.

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

You can explore the code and data for this project by clicking on the links provided above. For detailed insights, please refer to the [full blog post](https://github.com/marcusrprojects/What-Makes-Art-Valuable/blob/main/What%20Makes%20Art%20Valuable_%20Data%20Scraping%20and%20Exploratory%20Data%20Visualizations.pdf).
