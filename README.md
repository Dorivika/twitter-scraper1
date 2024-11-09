# Twitter Scraper

A Python-based tool for scraping tweets based on search terms using Microsoft Edge WebDriver and Selenium.

## Features

- Search Twitter for specific terms
- Scroll through and collect tweets automatically
- Extract tweet data including:
  - Username
  - Handle
  - Timestamp
  - Tweet text
  - Reply count
  - Retweet count
  - Like count
- Export data to CSV format

## Prerequisites

- Python 3.x
- Microsoft Edge browser
- Microsoft Edge WebDriver
- Required Python packages:
  ```
  selenium
  msedge-selenium-tools
  ```

## Installation

1. Install the required Python packages:
   ```bash
   pip install selenium msedge-selenium-tools
   ```

2. Download Microsoft Edge WebDriver:
   - Visit the [Microsoft Edge WebDriver Downloads](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/)
   - Download the version that matches your Edge browser
   - Add the WebDriver to your system PATH

## Usage

1. Run the script and enter your search term when prompted:
   ```python
   python twitter_scraper.py
   ```

2. The script will:
   - Open Microsoft Edge browser
   - Navigate to Twitter's search page
   - Enter your search term
   - Switch to the "Latest" tweets tab
   - Automatically scroll and collect tweets
   - Save the data to a CSV file named 'turkcell_tweets.csv'

## Code Structure

The script consists of three main components:

1. `get_tweet_data(card)`: Extracts data from individual tweet cards
   - Parses username, handle, date, text, and engagement metrics
   - Returns a tuple containing all tweet data

2. Search setup:
   - Initializes the Edge WebDriver
   - Navigates to Twitter
   - Performs the search

3. Data collection:
   - Scrolls through tweets
   - Collects unique tweets
   - Exports data to CSV

## Output Format

The script generates a CSV file with the following columns:
- UserName
- Handle
- Timestamp
- Text
- Comments
- Likes
- Retweets

## Limitations

- Requires Microsoft Edge browser
- No authentication support (only public tweets)
- May be affected by Twitter's rate limiting
- Subject to Twitter's layout changes

## Error Handling

The script includes basic error handling for:
- Missing tweet elements
- Scroll failures
- Web element location failures

## Contributing

Feel free to fork this repository and submit pull requests for any improvements.

## License

This project is open-source and available under the MIT License.

## Disclaimer

Please ensure you comply with Twitter's Terms of Service and rate limiting policies when using this scraper.
