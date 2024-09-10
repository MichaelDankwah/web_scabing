# Trustpilot Reviews Scraper

This repository contains a Python script for scraping reviews from Trustpilot for a specified company. The script leverages `BeautifulSoup` to extract user reviews, ratings, review dates, user locations, and other relevant information from the Trustpilot website. The scraped data is stored in a CSV file for easy analysis.

## Features

- **Extract user information:** Scrapes usernames, total reviews by the user, and user locations.
- **Review ratings and dates:** Extracts the rating (out of 5 stars) and the date the review was posted.
- **Review content:** Collects the full text of each review.
- **Data storage:** Outputs the scraped data into a structured CSV file.
- **Page navigation:** Scrapes reviews across multiple pages by iterating through paginated Trustpilot results.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Python 3.x](https://www.python.org/downloads/)
- [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
- [Requests](https://docs.python-requests.org/en/master/)
- [Pandas](https://pandas.pydata.org/)

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/web_scraping.git
2. Navigate to the project directory:

    ```bash
    cd web_scraping
3. Modify the following variables in the script:

- `company`: The Trustpilot URL slug for the company whose reviews you want to scrape (e.g., `backmarket.co.uk`).
- `from_page`: The page number to start scraping from.
- `to_page`: The page number to stop scraping.
4. Run the script

    ```bash
    python trustpilot_scraper.py
5. The script will save the extracted data into a CSV file named after the company:
   
    ```bash
    backmarket.co.uk_reviews.csv
    
## Notes

- **Rate-limiting**: The script includes a 2-second delay between each page scrape to avoid getting blocked by Trustpilot's rate limits. If you encounter connection issues, consider increasing the delay or using proxies.
- **HTML Structure**: Trustpilot's website structure might change over time, potentially breaking the scraping selectors. If this occurs, update the BeautifulSoup selectors in the code.
- **Terms of Service**: Please ensure that scraping the Trustpilot website complies with their terms of service.
