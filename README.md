# Selenium Web Scraper for H&M

This Python script utilizes Selenium to scrape product data from the H&M website. The script loads a collection URL, clicks the "Load More" button until no more products are loaded, and then extracts information such as product title, price, image URL, product URL, and available colors. The extracted data can be saved either into a database, MongoDB, or an Excel file.

### Prerequisites

- Python 3.x
- Selenium library
- Chrome WebDriver (Download and set the path to the executable in `DRIVER_FILE_PATH`)
- Pandas library (if saving data to an Excel file)
- pymongo library (if saving data to MongoDB)

### Installation

1. Install the required libraries:

```bash
pip install selenium
pip install pandas
pip install pymongo
```

2. Download the Chrome WebDriver from the official website: https://sites.google.com/a/chromium.org/chromedriver/downloads

### Usage

1. Open a Python environment or a Jupyter Notebook.

2. Copy the script to the environment.

3. Set the correct path to the Chrome WebDriver in the `DRIVER_FILE_PATH` variable.

4. Execute the script.

### Script Description

The script follows the following steps:

1. Initializes the Selenium WebDriver with optional headless mode.
2. Loads the H&M collection URL (`collection_url`).
3. Clicks the "Load More" button until all products are loaded on the page.
4. Extracts product data such as title, price, image URL, product URL, and available colors.
5. Creates a list of dictionaries, each containing the product information.
6. Depending on your choice:
   - If saving to MongoDB, the script uses `pymongo` to establish a connection and inserts the data into a specified collection.
   - If saving to an Excel file, the script creates a Pandas DataFrame with the extracted data and saves it to "h&m.xlsx" in the current directory.# HM-selenium-scraper
