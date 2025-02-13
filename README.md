# AI-website-summariser

## Overview
This project is a Python-based tool that scrapes the content of a given website, processes the text, and generates a concise summary using OpenAI's GPT-4o-mini model. It utilizes `requests` and `BeautifulSoup` to extract relevant content while ignoring navigation elements, scripts, styles, and images. The summarized output is displayed in markdown format using `rich`.

## Features
- **Website Scraping**: Uses `BeautifulSoup` to extract meaningful text from a webpage.
- **OpenAI GPT-4o-mini Integration**: Generates concise summaries based on extracted website content.
- **Rich Markdown Output**: Displays the summary in a readable markdown format using `rich`.
- **.env Support**: Loads API keys securely from a `.env` file.
- **Basic API Key Validation**: Checks for valid API key formats and warns the user if there are issues.

## Installation
### Prerequisites
Ensure you have Python 3 installed and then install the required dependencies:

```sh
pip install openai rich bs4 requests python-dotenv
```

## Setup
1. **Obtain an OpenAI API Key**:
   - Sign up at [OpenAI](https://openai.com/) and generate an API key.
   - The key should begin with `sk-proj-`.

2. **Create a `.env` file** in the root directory and add:
   ```sh
   OPENAI_API_KEY=your_api_key_here
   ```

## Usage
Run the script to summarize a webpage:

```sh
python script.py
```

### Code Structure
- `Website` class:
  - Fetches and parses the HTML content of a webpage.
  - Extracts and cleans up the main text content.
- `summarise(url)`: Calls OpenAI's GPT API to generate a summary of the webpage.
- API Key Validation:
  - Ensures the correct format and warns users of potential issues.
- Output:
  - The summary is printed in markdown format to the console using `rich`.

## Example Output
```
# Summary of Lost Pet Flyers
Lost Pet Flyers is a website dedicated to helping reunite lost pets with their owners...
```

## Troubleshooting
If you encounter issues:
- **Missing API key**: Ensure your `.env` file contains a valid OpenAI key.
- **Invalid API key format**: Double-check that the key starts with `sk-proj-`.
- **No content extracted**: Some websites block scraping; try a different URL.

## License
This project is open-source under the MIT License.

## Contributions
Pull requests and improvements are welcome!

