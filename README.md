                              NSE Equity Statistics Scraper

This project automates the process of scraping Nairobi Securities Exchange (NSE) equity statistics from the official NSE website. The script uses Python + Selenium to collect data across all market sectors and save it into a structured CSV file.

The end goal of this project is not just to fetch data, but also to analyze it so you can make better-informed investment decisions, such as identifying which shares to buy.

                                 Features

Automatically opens the NSE Market Statistics page.

Navigates to the Equity Statistics tab.

Iterates through all market sectors in the dropdown.

 Extracts the following information for each listed company:

Company Name

ISIN Code

Volume

Last Traded Price

Price Change

Sector

Saves all the data to a CSV file (AllShares.csv).

                   Tech Stack

Python 3.9+

Selenium (web scraping automation)

webdriver-manager (auto-downloads ChromeDriver)

Google Chrome browser

Numpy

                   How to run the code
    Install Python
Make sure you have Python 3.8 or later installed.
You can check by running:



Install Google Chrome
The script uses Chrome with Selenium, so you need Google Chrome installed.

Install ChromeDriver

Go to ChromeDriver Downloads

Download the version that matches your Chrome browser version

Place the executable in your PATH (so Python can find it), or in the same folder as your script.

Install dependencies
selenium
numpy
Jupyter


