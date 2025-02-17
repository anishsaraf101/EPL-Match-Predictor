# Premier League Match Prediction

This is a solo project that scrapes Premier League match data from [FBRef.com](https://fbref.com) and trains a Random Forest Classifier to predict match outcomes. The project consists of two main Jupyter notebooks:

- **`EPL_scraping.ipynb`** – Scrapes match data from FBRef and compiles it into a CSV file.
- **`EPL_prediction.ipynb`** – Prepares the dataset, trains a machine learning model, and evaluates its accuracy.

## Project Overview

### 1. Data Scraping

The `EPL_scraping.ipynb` file performs web scraping using `requests` and `BeautifulSoup`. It:

- Fetches the Premier League standings page.
- Extracts links to individual team pages.
- Scrapes match results, fixtures, and statistical data.
- Converts the extracted tables into a Pandas DataFrame and saves them as `combined_file.csv`.

### 2. Data Processing and Model Training

The `EPL_prediction.ipynb` file processes the scraped data and trains a machine learning model. It:

- Loads `combined_file.csv` and preprocesses the data (converts dates, encodes categorical features, extracts relevant predictors).
- Defines the `target` variable (win = 1, loss/draw = 0).
- Splits the data into training (before 2023) and testing (after 2023) sets.
- Trains a `RandomForestClassifier` with selected predictors.
- Evaluates the model using accuracy score.

## Installation and Usage

### Prerequisites

Ensure you have the following Python libraries installed:

```bash
pip install pandas requests beautifulsoup4 scikit-learn
```


## Running the Project

1. Run `EPL_scraping.ipynb` to fetch and save match data.
2. Run `EPL_prediction.ipynb` to train the model and predict match results.

## Results

The current model achieves around **66% accuracy** in predicting match outcomes.

## License

This project is open-source and available under the MIT License.

