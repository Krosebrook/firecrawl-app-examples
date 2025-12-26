# Documentation RAG System

A system for scraping, processing, and managing documentation for RAG (Retrieval-Augmented Generation) applications using DeepSeek R1, Ollama, Streamlit and Firecrawl.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)

## Features

- **Documentation Scraping**: Automatically scrapes documentation from specified URLs
- **Flexible Storage**: Stores documentation in organized directory structures
- **Streamlit Interface**: User-friendly web interface for managing documentation
- **Configurable Scraping**: Control the number of pages scraped and documentation naming

## Use Cases

1. **Developer Documentation Assistant**: Build a RAG system that answers questions about specific frameworks, libraries, or APIs using their official documentation.

2. **Internal Knowledge Base**: Scrape and organize company documentation, wikis, and internal resources for AI-powered employee assistance systems.

3. **Technical Support Automation**: Create intelligent support bots that can reference product documentation to provide accurate answers to customer queries.

4. **Learning Path Generator**: Extract educational content from multiple documentation sources to create personalized learning paths and study materials.

## Prerequisites

Before setting up the project, ensure you have:

- Python 3.x installed
- A Firecrawl account (sign up at <https://firecrawl.dev> and get your API key)
- Environment variables properly configured (see `.env.example` file)
- Ollama installed and running ([download instructions](https://ollama.com/download/mac)):

1. Install Ollama

```bash
brew install ollama
```

2. Start the Ollama server

```bash
ollama serve
```

3. Pull the required model used in the repository

```bash
# 14 billion parameters
ollama pull deepseek-r1:14b 
```

If you have strong enough hardware, try bigger versions of the DeepSeek R1 model as model size significantly affects performance.

## Installation

1. Clone the repository:

```bash
git clone https://github.com/BexTuychiev/local-documentation-rag.git
cd local-documentation-rag
```

2. Install required dependencies:

```bash
pip install -r requirements.txt
```

3. Create a `.env` file in the project root and configure required environment variables.

## Usage

1. Start the Streamlit application:

```bash
streamlit run src/app.py
```

2. Through the web interface, you can:
   - Configure documentation scraping
   - Specify base URLs for documentation
   - Control the number of pages to scrape

### Documentation Naming Conventions

- Documentation directories must end with `-docs` suffix
- Names should be descriptive and relate to the documentation being scraped
- Example: `Firecrawl-docs`, `API-docs`

## Features in Detail

### Documentation Scraping

The system provides a robust scraping mechanism that:

- Handles various documentation formats
- Maintains proper directory structure
- Supports pagination and depth control
- Provides progress feedback

### RAG Integration

The system is designed to work with RAG applications by:

- Converting documentation to appropriate formats
- Maintaining proper data structure for retrieval
- Supporting various documentation sources
