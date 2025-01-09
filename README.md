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


### Customizing the Scraper

#### 1. Target Product or Category
You can scrape different products or categories by modifying the `FLIPKART_URL` variable in the code. For instance:
- Change the URL to target a specific search query, such as "laptops" or "headphones."
- Use category-specific URLs to narrow down the results (e.g., "Samsung smartphones" or "4K TVs").

#### 2. Extract Additional Fields
Enhance the scraper by modifying the HTML parsing logic to extract more details from the product listings. Additional fields you might want to include:
- **Discounts**: Extract the percentage or amount saved on each product.
- **Delivery Options**: Scrape information about delivery times or charges.
- **Seller Information**: Get details about the seller (e.g., name or rating).
- **Stock Availability**: Check if the product is in stock or out of stock.

#### 3. Pagination
To scrape data from multiple pages of results, implement a loop in the code to navigate through Flipkart's paginated results:
- Flipkart URLs for paginated results typically include a page number parameter, such as `page=2` or `page=3`.
- Modify the scraper logic to iterate through these page numbers until all relevant data is collected.

**Example:**
```python
base_url = "https://www.flipkart.com/search?q=samsung+phones&page="
for page in range(1, 6):  # Scrape first 5 pages
    url = f"{base_url}{page}"
    response = requests.get(url)


