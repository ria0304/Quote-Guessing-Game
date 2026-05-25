# 📖 Quote Guessing Game

> A Python web-scraping game powered by [quotes.toscrape.com](http://quotes.toscrape.com)

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square&logo=python)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Attempts](https://img.shields.io/badge/Attempts-4%20per%20game-orange?style=flat-square)
![Difficulty](https://img.shields.io/badge/Hints-Progressive-purple?style=flat-square)

---

## Overview

Quote Guessing Game is a command-line Python application that scrapes real quotes from `quotes.toscrape.com` and turns them into an interactive guessing challenge. Each session randomly selects a quote and asks you to name the author — with progressively revealing hints after every wrong answer.

---

## How It Works

1. Sends paginated HTTP requests to `quotes.toscrape.com`
2. Parses HTML with BeautifulSoup to extract quotes, authors, and biography links
3. Stores all data in structured Python dictionaries
4. Randomly picks one quote to present per session
5. Prompts the user for up to **4 guesses**, releasing a new hint after each miss
6. Ends on a correct guess or when all attempts are exhausted

---

## Features

| Feature | Description |
|---|---|
| Multi-page scraping | Automatically follows pagination and collects quotes from all available pages |
| Structured data storage | Each quote is stored with its text, author name, and biography URL |
| Random quote selection | A new quote is chosen at random each session for replay variety |
| 4-attempt limit | Players have up to four chances before the answer is revealed |
| Progressive hints | Hints unlock sequentially to help without spoiling the answer |
| Ethical scraping delays | Uses `time.sleep()` between requests to respect the source server |

### 💡 Progressive Hint System

| Attempt | Hint Revealed |
|---|---|
| 1st guess | No hints — just the quote |
| 2nd guess | Author's birth date and location |
| 3rd guess | First name initial |
| 4th guess | Last name initial |

---

## Technologies Used

| Library | Purpose |
|---|---|
| `requests` | Handles HTTP GET requests to fetch page HTML |
| `beautifulsoup4` | Parses and navigates HTML to extract quotes and metadata |
| `random` | Selects a random quote from the scraped dataset |
| `time` | Introduces polite delays between requests |

---

## Project Structure

```
quote-guessing-game/
│
├── quote_game.py       ← Main script (scraping + game logic)
└── README.md           ← Project documentation
```

---

## Installation

### Prerequisites

- Python 3.x
- pip (bundled with Python 3.4+)

### Install Dependencies

```bash
pip install requests beautifulsoup4
```

---

## Usage

Run the script from your terminal:

```bash
python quote_game.py
```

Follow the on-screen prompts to guess the author of the displayed quote.

---

## Example Output

```
Here's a quote:

"Life is what happens to us while we are making other plans."

Who said this quote? Guesses remaining: 4
> John Lennox

Incorrect! Hint: Born June 23, 1912 in Maida Vale, London.
Who said this quote? Guesses remaining: 3
> John Lennon

Incorrect! Hint: First name starts with "A"
Who said this quote? Guesses remaining: 2
> Allen Saunders

Correct! The quote was by Allen Saunders. Well done!
```

---

## Ethical Scraping Notice

This project targets `quotes.toscrape.com`, a site built specifically for scraping practice. The script includes deliberate time delays between requests to minimise server load. Please do not remove these delays or use this script against sites that do not permit scraping.

---

## Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/my-feature`
3. Commit your changes: `git commit -m 'Add my feature'`
4. Push to the branch: `git push origin feature/my-feature`
5. Open a Pull Request

---

## License

This project is licensed under the [MIT License](LICENSE).

---

