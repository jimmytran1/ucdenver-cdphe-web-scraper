# Python Web Scraper (UCD + Colorado COVID Data)

A simple Python web scraping script with a CLI menu that lets you run two scrapers:

1. **UCD Web Scraping**  
   Scrapes the University of Colorado Denver welcome page and extracts `application/ld+json` structured data. It then pulls the **department name, telephone, and URL** (if present) and saves the results to `output.json`.

2. **COVID-19 Web Scraping**  
   Scrapes the Colorado Department of Public Health and Environment (CDPHE) COVID-19 data page, extracts table rows (`<tr>` / `<td>`), converts them into a **Pandas DataFrame**, and displays the results as an **HTML table** (best used in Jupyter / IPython).

---

## Features

- Command-line menu to choose which scraper to run
- Uses `requests` with a browser-like User-Agent
- Parses HTML with `BeautifulSoup`
- UCD scraper:
  - Reads structured data from `<script type="application/ld+json">`
  - Extracts department fields and writes them to `output.json`
- COVID scraper:
  - Extracts table data and renders it via Pandas as HTML

---

## Requirements

- Python 3.9+ recommended

Install dependencies:

```bash
pip install requests beautifulsoup4 pandas ipython
