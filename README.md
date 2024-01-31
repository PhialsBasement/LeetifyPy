# Leetify Web Scraping Library
===========================

The LeetifyPy Library is a Python package designed to facilitate the extraction of player data from the popular gaming platform Leetify. Leveraging the power of Selenium, this library provides a seamless interface to retrieve essential information about players, including their names, win rates, and teammate details.

# Features
--------

- **Get Player Name:** Extract the player name associated with a given account link on Leetify. The library navigates through the website's structure, locating the relevant elements and delivering accurate player names.

- **Get Player Win Rate:** Retrieve the win rate percentage of a player by supplying their Leetify account link. The library navigates dynamically loading pages, ensuring accurate and up-to-date win rate information.

- **Get Player Teammates:** Collect a dictionary of a player's teammates and their respective Leetify account links. The library intelligently identifies and fetches this data, providing a comprehensive overview of a player's gaming network.

# Usage
-----

To use the Leetify Web Scraping Library, install it using pip:

```bash
pip install LeetifyPy
```
Then, in your Python code, import the library and create an instance of the WebScraper class

```bash
from leetify_web_scraper.scraper import WebScraper

scraper = WebScraper()
```

From here you can utilise the functions as so

```bash
account_link = "https://leetify.com/player/123"

# Get Player Name
player_name = scraper.get_player_name(account_link)
print(f"Player Name: {player_name}")

# Get Player Win Rate
win_rate = scraper.get_player_winrate(account_link)
print(f"Win Rate: {win_rate}")

# Get Player Teammates
teammates = scraper.get_player_teammates(account_link)
print("Teammates:")
for teammate, teammate_link in teammates.items():
    print(f"{teammate}: {teammate_link}")
```
