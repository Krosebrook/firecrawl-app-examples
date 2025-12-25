# Automated Price Tracking System

A robust price tracking system that monitors product prices across e-commerce websites and notifies users of price changes through Discord.

## Features

- Automated price checking every 6 hours
- Support for multiple e-commerce platforms through Firecrawl API
- Discord notifications for price changes
- Historical price data storage in PostgreSQL database
- Interactive price history visualization with Streamlit

## Use Cases

1. **Smart Shopping**: Track prices of wish-list items across multiple retailers and get notified when they drop below your target price, never missing a good deal.

2. **Competitive Pricing Analysis**: Businesses can monitor competitor pricing in real-time to adjust their own pricing strategies and maintain market competitiveness.

3. **Inventory Management**: Retailers can track supplier prices to optimize procurement timing and negotiate better deals when prices are favorable.

4. **Price History Analysis**: Identify seasonal pricing patterns and optimal purchase times for specific product categories by analyzing historical price data.

## Setup

1. Clone the repository
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Configure environment variables:

   ```bash
   cp .env.example .env
   ```

   Then edit `.env` with your:
   - Discord webhook URL
   - Database credentials
   - Firecrawl API key
