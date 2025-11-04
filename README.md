# 🛰️ SpaceX Launch Data Analysis

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup4-Web%20Scraping-brightgreen)](https://pypi.org/project/beautifulsoup4/)
[![pandas](https://img.shields.io/badge/pandas-Data%20Analysis-150458?logo=pandas)](https://pandas.pydata.org/)
[![matplotlib](https://img.shields.io/badge/matplotlib-Visualization-orange?logo=plotly)](https://matplotlib.org/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/Status-Active-success)]()
[![Last Commit](https://img.shields.io/github/last-commit/yourusername/SpaceX-Launch-Parser)]()

---

## 🚀 Overview
**SpaceX Launch Data Analysis** is a Python-based project that scrapes, cleans, and visualizes detailed launch records of **Falcon 9** and **Falcon Heavy** rockets from Wikipedia.  
The project demonstrates an **end-to-end data workflow**: scraping → cleaning → structuring → visualization.  

This repository is perfect for:
- Learning **web scraping and HTML parsing**
- Exploring **semi-structured data cleaning**
- Conducting **exploratory data analysis (EDA)**
- Building **publication-ready visualizations**

---

## 🌐 Data Source
- Wikipedia: [List of Falcon 9 and Falcon Heavy launches](https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches)
- Tables often include annotations, missing values, and symbols like `[8]` or `♺`.  
- The scraper handles inconsistencies and creates a clean dataset.

---

## ⚙️ Methodology

### 1️⃣ Data Extraction
- Scrapes all `<table>` elements with the class `wikitable plainrowheaders collapsible`.
- Iterates through each row (`<tr>`) to identify valid launch records.
- Extracts fields such as `Flight No.`, `Date`, `Version Booster`, `Launch Site`, `Payload`, `Orbit`, `Customer`, `Launch outcome`, and `Booster landing`.

### 2️⃣ Data Cleaning
- Regex removes references `[a]`, `[8]`, and symbols like `♺`.
- Missing or inconsistent values handled gracefully.
- Units standardized (payload mass in kg).

### 3️⃣ Data Structuring
- Data stored in a Python dictionary (`launch_dict`) → converted to `pandas.DataFrame`.
- Exported as:
