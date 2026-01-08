Quote Guessing Game using Web Scraping
Overview
This project is a Python-based web scraping application that collects quotes from the website quotes.toscrape.com and turns them into an interactive command-line guessing game.
The program scrapes quotes from multiple pages, randomly selects one quote, and asks the user to guess the author. If the user answers incorrectly, progressive hints are provided to help identify the author.

Features
Scrapes quotes from multiple pages automatically
Extracts quote text, author name, and author biography link
Stores scraped data in structured Python dictionaries
Randomly selects a quote for each game session
Allows up to four guessing attempts
Provides hints after each incorrect guess:
Author birth date and location
First name initial
Last name initial
Uses request delays to follow ethical scraping practices

Technologies Used
Python 3
requests
BeautifulSoup (bs4)
time
random

Project Structure
quote-guessing-game/
│
├── quote_game.py
└── README.md

How It Works
The program sends HTTP requests to quotes.toscrape.com

HTML content is parsed using BeautifulSoup

Quotes are extracted from all paginated pages

A random quote is selected from the scraped data

The user is prompted to guess the author

Additional hints are shown after incorrect guesses

The game ends when the correct answer is given or attempts are exhausted

Installation
Prerequisites
Python 3.x installed on your system
Install Dependencies
pip install requests beautifulsoup4
Usage
Run the Python script from the terminal:
python quote_game.py
Follow the on-screen instructions to play the game.

Example Output
Here's a quote:
"Life is what happens to us while we are making other plans."
Who said this quote? Guesses remaining 4:
Hints are displayed after each incorrect attempt.

