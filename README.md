# Web Scraping & Lead List Automation

Python tool that automatically collects structured business contact
information from a public online professional directory, replacing
slow and error-prone manual copy-pasting.

## What it does
- Uses Selenium to open the directory and move through all result pages
  by clicking the "next" button
- Parses page HTML with BeautifulSoup to find each listing block
- Extracts name, address, city, state, ZIP code, phone, email and website
  using regular expressions
- Detects the company name from the website or email domain (ignores free
  providers such as Gmail and Yahoo), with a keyword-based fallback
- Filters out irrelevant records (.edu emails, listings without address)
- Removes duplicates with Pandas and exports a clean Excel file

## Tools
Python, Selenium, BeautifulSoup, Pandas, Regex

## How to run
1. pip install selenium webdriver-manager beautifulsoup4 pandas openpyxl
2. Run the script, select a category on the website and submit
3. Press ENTER in the terminal when the results page is loaded
4. The script collects all pages and saves an Excel file

## Marketing use cases
Lead generation, competitor and market research, building buyer or
supplier databases.

## Limitations and future improvements
- Category selection is manual; it could be automated
- Replace fixed waits with explicit waits
- Add error logging

## Note
Only publicly listed business information is collected. No data files
are included in this repository. Please check a website's terms of use
before scraping.
