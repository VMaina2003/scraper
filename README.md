# NSE Equity Statistics Scraper

A Python-based web scraping tool that automates the collection of Nairobi Securities Exchange (NSE) equity statistics from the official NSE website.

The scraper uses **Selenium + ChromeDriver** to navigate through all listed market sectors, extract equity data, and save it into a structured CSV file. After scraping, it performs a basic analysis of gainers, losers, and most traded stocks, helping investors identify potential opportunities.

---

## Features

- Automatically opens the NSE Market Statistics page  
- Navigates to the **Equity Statistics** tab  
- Iterates through all available market sectors  
- Extracts the following information for each company:  
  - Sector  
  - Company Name  
  - Share Code  
  - Volume  
  - Last Traded Price  
  - Price Change  
- Saves all extracted data into **`equity_all_sectors.csv`**  
- Runs a quick analysis:
  - Top 5 Gainers  
  - Top 5 Losers  
  - Most Traded Stocks  
  - Best Probable Buys (based on momentum + liquidity)  

---

## Tech Stack

- Python 3.9+  
- Selenium (browser automation)  
- webdriver-manager (auto-handles ChromeDriver)  
- Google Chrome (latest stable version recommended)  
- Pandas & NumPy (data cleaning and analysis)  

---

## Installation & Setup

### 1. Clone the repository

git clone https://github.com/your-username/nse-equity-scraper.git
cd nse-equity-scraper
2. Create a virtual environment (recommended)
bash
Copy code
python -m venv venv
# Mac/Linux
source venv/bin/activate
# Windows
venv\Scripts\activate
3. Install dependencies
bash
Copy code
pip install -r requirements.txt
The requirements.txt file should include:

nginx
Copy code
selenium
pandas
numpy
webdriver-manager
4. Ensure Google Chrome is installed
Check your Chrome version:

Open Chrome → navigate to chrome://settings/help

The correct ChromeDriver will be downloaded automatically by webdriver-manager.

How to Run
bash
Copy code
python main.py
The script will:

Launch Chrome in automated mode

Navigate through all NSE equity sectors

Save the scraped results into equity_all_sectors.csv

Print summary statistics (top gainers, losers, most traded, and probable buys)

Output
CSV file: equity_all_sectors.csv

Example columns:

text
Copy code
Sector, Company, Share Code, Volume, Last Traded Price, Change ($)
BANKING, Equity Group Holdings, EQTY, 1,200,000, 38.50, +0.45
MANUFACTURING, BAT Kenya, BAT, 300,000, 420.00, -5.00
Console Output:

text
Copy code
Top 5 Gainers:
        Company        Sector     Change ($)    Volume
...

Best Probable Buys (Momentum + Liquidity):
        Company        Sector     Change ($)    Volume    Score
...
Notes & Limitations
The NSE website may change its structure, which could break the scraper

Long runtime if internet connection is slow (script waits for pages to load)

Best used as a data collection + quick analysis tool — not financial advice

Roadmap / Future Improvements
 Add scheduling for daily automatic scraping

 Export results to Excel or Google Sheets

 Build a simple dashboard (Streamlit/Flask) for visualization

 Integrate notifications (email/Telegram) for top gainers/losers

License
MIT License – feel free to use and modify.

pgsql
Copy code
