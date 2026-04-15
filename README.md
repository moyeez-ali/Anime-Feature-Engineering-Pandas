# Anime Dataset: Feature Extraction & Text Parsing

## Project Overview
This project focuses on transforming messy, unstructured text data into clean, analytically viable features. Using a raw dataset of top-rated anime, the primary objective was to parse complex, concatenated string columns to extract specific numerical and temporal data points. This allowed for deeper exploratory data analysis and specific querying.

## Technologies Used
* **Language:** Python 3
* **Libraries:** Pandas, `datetime`, `dateutil`
* **Environment:** Jupyter Notebook

## Key Feature Engineering Tasks
1. **Custom String Parsing:** Developed custom Python functions to iterate through dense text strings and extract episode counts hidden within parentheses (e.g., isolating "64" from "BrotherhoodTV (64 eps)Apr 2009").
2. **Data Type Conversion:** Cleaned the extracted text by stripping string literal remnants (`" eps"`) and casting the data into integer types for mathematical operations.
3. **Temporal Data Extraction:** Engineered logic to slice string indices and isolate specific start and end airing dates from unformatted text blocks.
4. **Time-Series Calculations:** Utilized `datetime` and `dateutil.relativedelta` to compute the exact total broadcast duration of each show in months, creating a brand-new `Months` feature for analysis.

## Key Insights Extracted
Once the features were engineered, the dataset was queried to find specific benchmarks:
* **Highest Rated Anime:** *Fullmetal Alchemist: Brotherhood* achieved the maximum score (9.10).
* **Maximum Episodes:** *Gintama* topped the list with the highest episode count (201 episodes) among the top records.
* **Longest Running Anime:** *Ginga Eiyuu Densetsu* holds the record for the longest continuous runtime (111 months).

## How to Run the Project
1. Clone this repository to your local machine.
2. Ensure you have Python and Pandas installed (`pip install pandas python-dateutil`).
3. Open the `feature.extraction.project.ipynb` file using Jupyter Notebook or your preferred IDE.
4. Run the cells sequentially to observe the step-by-step string manipulation and data querying process.

## 👨‍💻 Author
**Syed Moyeez Ali** Data Science Enthusiast | Exploring Data Wrangling & Feature Engineering
