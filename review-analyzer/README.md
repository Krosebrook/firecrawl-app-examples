# Review Analyzer

A Streamlit application that scrapes and analyzes product reviews using OpenAI's GPT model.

## Setup

1. Clone the repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up environment variables:
   - Copy `env.example` to `.env`:
     ```bash
     cp env.example .env
     ```
   - Edit `.env` and add your API keys:
     - `OPENAI_API_KEY`: Your OpenAI API key
     - `FIRECRAWL_API_KEY`: Your Firecrawl API key

## Running the Application

Start the Streamlit app:
```bash
streamlit run app.py
```

The application will be available at `http://localhost:8501`

## Features

- Scrapes product reviews from Amazon
- Analyzes reviews using OpenAI's GPT model
- Extracts meaningful pros and cons
- Presents analysis in a clean, organized format

## Use Cases

1. **Purchase Decision Support**: Quickly analyze hundreds of product reviews to make informed buying decisions without reading every review manually.

2. **Product Research**: Researchers and analysts can gather sentiment data and common feedback themes from large sets of customer reviews.

3. **Competitive Product Analysis**: Businesses can analyze competitor product reviews to identify gaps in the market and improvement opportunities.

4. **E-commerce Optimization**: Online sellers can track and analyze their product reviews to identify common issues and improve product descriptions or features.

## Environment Variables

- `OPENAI_API_KEY`: Required. Your OpenAI API key for review analysis
- `FIRECRAWL_API_KEY`: Required. Your Firecrawl API key for web scraping
- `ENVIRONMENT`: Optional. Set to 'development' or 'production' (default: development)
- `DEBUG`: Optional. Set to 'true' to enable debug logging (default: false)

## Project Structure

```
review-analyzer/
├── app.py              # Main Streamlit application
├── requirements.txt    # Python dependencies
├── env.example        # Example environment variables
└── src/
    ├── __init__.py
    ├── review_analyzer.py  # Review analysis using OpenAI
    └── scraper.py         # Web scraping functionality
``` 