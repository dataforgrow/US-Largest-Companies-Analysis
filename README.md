# US Largest Companies by Revenue and Profit

This project involves web scraping data from Wikipedia to create a dataset of the largest companies in the United States by revenue and profit. It leverages Python libraries like `BeautifulSoup` for web scraping and `pandas` for data manipulation and analysis.

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Setup](#setup)
- [Data Extraction](#data-extraction)
- [Data Analysis](#data-analysis)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

The goal of this project is to collect and analyze data on the largest public and private companies in the United States, as well as the most profitable companies, based on information available on Wikipedia. The collected data is then organized into pandas DataFrames for easy access and further processing.

## Data Sources

The primary data source for this project is the Wikipedia page:
[List of largest companies in the United States by revenue](https://en.wikipedia.org/wiki/List_of_largest_companies_in_the_United_States_by_revenue)

## Setup

To run this project, you will need Python installed. We recommend using a virtual environment.

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. Install the required Python packages:
   ```bash
   pip install beautifulsoup4 requests pandas
   ```

## Data Extraction

The data extraction process involves:

1. **Fetching the Web Page**: Using the `requests` library to download the content of the Wikipedia page.
2. **Parsing with BeautifulSoup**: Utilizing `BeautifulSoup` to parse the HTML content and locate the relevant tables containing company data.
3. **Identifying Tables**: Extracting three main tables:
    - List of the largest public / publicly traded companies
    - List of largest private companies
    - List of companies by profit
4. **Populating DataFrames**: Iterating through the rows and columns of each table to extract data and store it into separate pandas DataFrames.

## Data Analysis

After extraction, the data is available in three pandas DataFrames:

- `df`: Contains data for the largest public / publicly traded companies.
- `dfp`: Contains data for the largest private companies.
- `dfp1`: Contains data for the most profitable companies.

These DataFrames can then be used for various analyses, such as:

- Sorting companies by revenue, profit, or number of employees.
- Analyzing industry distribution among top companies.
- Identifying headquarters locations of major corporations.

## Usage

To recreate the data extraction and analysis:

1. Open the Jupyter Notebook (or Google Colab notebook) provided in this repository.
2. Run the cells sequentially to perform web scraping and data loading into DataFrames.
3. Explore the `df`, `dfp`, and `dfp1` DataFrames to access the extracted information.

Example of accessing data:

```python
import pandas as pd

# Assuming df is already populated from the scraping steps
print("Top 5 Public Companies by Revenue:")
print(df.head())

# Assuming dfp is already populated
print("\nLargest Private Companies:")
print(dfp)

# Assuming dfp1 is already populated
print("\nMost Profitable Companies:")
print(dfp1)
```

## Contributing

Feel free to fork this repository and contribute by improving the scraping logic, adding more analysis, or enhancing the documentation.

## License

This project is open-source and available under the [MIT License](LICENSE).
