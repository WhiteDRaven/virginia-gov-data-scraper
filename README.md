# Web Scraper & Automated Excel Reporter

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![Excel](https://img.shields.io/badge/Excel-Automation-success)

## Project Overview

This tool solves a common problem in data entry: **preserving hyperlinks when exporting web tables.**

Manual copy-pasting from websites often results in plain text, losing the underlying URLs (hyperlinks) which are critical for audits and research. This Python script automates the extraction process, capturing both visible text and hidden `href` attributes, and delivers a fully formatted, client-ready Excel report.

## Key Features

* **Smart Extraction:** Parses HTML tables (`<table>`) using `BeautifulSoup`.
* **Hidden Data Capture:** Automatically extracts `href` URLs from the first column and creates a dedicated "Source URL" column.
* **Data Cleaning:** Removes citation footnotes (e.g., `[1]`) and sanitizes text using `Pandas`.
* **Excel Automation:** Uses `XlsxWriter` to format the output as a **Native Excel Table** (blue theme, auto-filters enabled, and auto-adjusted column widths).
* **Ethical Scraping:** Includes User-Agent headers and rate limiting (`time.sleep`) to respect server load.

## Output Example

The script transforms raw HTML into a structured business report.

*(Place your "Split Screen" screenshot here: Code on the left, Excel Output on the right)*
![Images/Virginia_Gov_Data_Clean_View.PNG]

## Technologies Used

* **Python 3.x**
* **BeautifulSoup4** (HTML Parsing)
* **Pandas** (Data Manipulation)
* **XlsxWriter** (Excel Formatting)
* **Requests** (HTTP Connection)

## Installation & Usage

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/WhiteDRaven/virginia-gov-data-scraper.git](https://github.com/WhiteDRaven/virginia-gov-data-scraper.git)
    ```

2.  **Install dependencies:**
    ```bash
    pip install pandas requests beautifulsoup4 xlsxwriter
    ```

3.  **Run the script:**
    ```bash
    python scraper.py
    ```

4.  **Result:**
    A file named `Virginia_Gov_Data_Clean.xlsx` will be generated in the same folder.

## Ethical & Legal Compliance

This script is designed for educational and legitimate data analysis purposes using **Public Data** (Virginia Counties List / Government Records).
* It respects `robots.txt` policies.
* It identifies as a legitimate browser via `User-Agent`.
* It implements delays to prevent server overloading.

## Author

**Jonathan González**
*Data Analyst & Automation Expert*

Looking for a custom scraping solution?
https://freelancerprofilenuxt.mesh.prod.platform.usw2.upwork/freelancers/~01b91dfaecf1854135?mp_source=share