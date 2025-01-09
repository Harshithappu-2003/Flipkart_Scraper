# Flipkart Scraper

## Overview
This project provides a web scraping tool to extract details of Samsung phones listed on Flipkart. It uses Python libraries like `requests` and `BeautifulSoup` for sending HTTP requests and parsing HTML content. The project is designed to help users gather product data for analysis, comparison, or personal reference in a structured and efficient manner.

## Features
- **Product Details Scraping**: Fetches key information such as:
  - Product Name
  - Price
  - Specifications (e.g., features, storage options, etc.)
  - Ratings and Reviews (if available)
- **Customizable Target**: While this version is tailored for Samsung phones, the logic can be extended to scrape other categories like laptops, home appliances, or clothing by modifying URL parameters.
- **Robust Parsing**: Handles changes in Flipkart's webpage structure by using CSS selectors, making it adaptable to minor website updates.
- **Scalable Codebase**: Can be integrated into larger projects for e-commerce analysis or research.

## Prerequisites
Before running the scraper, ensure the following are set up on your system:

1. **Python 3.x Installed**:
   Install Python from the [official website](https://www.python.org/) if not already installed.

2. **Required Python Libraries**:
   - `requests`: To make HTTP requests and fetch web page content.
   - `beautifulsoup4`: For parsing and navigating HTML content.

   Install these libraries by running the following command:
   ```bash
   pip install requests beautifulsoup4

## Example Output

The scraper fetches and displays product details in a structured tabular format. Below is an example of the extracted data:

| Product Name            | Price      | Specifications        | Ratings | Reviews |
|-------------------------|------------|-----------------------|---------|---------|
| Samsung Galaxy S23 Ultra| ₹1,24,999  | 12GB RAM, 256GB Storage | 4.8     | 3,204   |
| Samsung Galaxy A14      | ₹13,999    | 4GB RAM, 64GB Storage  | 4.5     | 1,128   |
| Samsung Galaxy M13      | ₹11,499    | 6GB RAM, 128GB Storage | 4.3     | 2,759   |
| Samsung Galaxy F54      | ₹21,999    | 8GB RAM, 128GB Storage | 4.7     | 1,453   |

### Key Fields
- **Product Name**: Name of the product as listed on Flipkart.
- **Price**: The listed price of the product in Indian Rupees.
- **Specifications**: Key technical details like RAM and storage capacity.
- **Ratings**: Average user rating out of 5.
- **Reviews**: Number of reviews provided by users.



