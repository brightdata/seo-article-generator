<div align="center">
<p align="center">
  <a href="https://brightdata.com/">
    <img src="https://mintlify.s3.us-west-1.amazonaws.com/brightdata/logo/light.svg" width="300" alt="Bright Data Logo">
  </a>
</p>

# AI-Powered Article Generator 

An intelligent content tool that scrapes Google, extracts live web data with Bright Data MCP, and uses AI to generate articles from real-time research.

<img src="https://img.shields.io/badge/python-3.8+-blue" /> <img src="https://img.shields.io/badge/Node.js-18+-success" /> <img src="https://img.shields.io/badge/License-MIT-blue" />

<img src="https://media.brightdata.com/2025/09/Demo-gif.gif" />
</div>

---

## Features

- 🔍 **SERP Scraping**: Automatically extract relevant URLs from Google search results
- 📄 **Content Extraction**: Scrape and clean content from web pages using Bright Data MCP tools
- 🧠 **AI Analysis**: Process content using OpenAI embeddings and vector similarity search
- ✍️ **Content Generation**: Create article outlines or full articles using LangChain and OpenAI
- 📊 **Research Metrics**: View detailed analysis of scraped content and identified themes

## Prerequisites

- Python 3.8+
- OpenAI API key
- Bright Data API token
- Node.js (for MCP tools)

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd article-generator
   ```

2. **Install Python dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Install Node.js MCP tools**
   ```bash
   npx @brightdata/mcp
   ```

4. **Set up environment variables**
   
   Create a `.env` file in the project root:
   ```env
   OPENAI_API_KEY=your_openai_api_key_here
   BRIGHT_DATA_API_TOKEN=your_bright_data_api_token_here
   WEB_UNLOCKER_ZONE=your_web_unlocker_zone_here
   BROWSER_ZONE=your_browser_zone_here
   ```

## Usage

1. **Start the application**
   ```bash
   streamlit run article_generator.py
   ```

2. **Open your browser**
   
   The app will automatically open at `http://localhost:8501`

3. **Generate content**
   - Enter your research keyword (e.g., "artificial intelligence in healthcare")
   - Configure settings in the sidebar:
     - Maximum sources to scrape (5-20)
     - Output type (Article Outline or Full Article)
     - Target word count for full articles (800-3000)
   - Click "🚀 Generate Content"

## How It Works

1. **Search**: Scrapes Google search results for your keyword
2. **Extract**: Downloads and cleans content from relevant web pages
3. **Analyze**: Uses AI embeddings to identify key themes and insights
4. **Generate**: Creates structured content based on the research analysis

## Configuration

### Sidebar Options
- **Maximum sources**: Number of web pages to scrape (5-20)
- **Output type**: Choose between article outline or full article
- **Target word count**: Desired length for full articles (800-3000 words)

### Environment Variables
- `OPENAI_API_KEY`: Your OpenAI API key for content generation
- `BRIGHT_DATA_API_TOKEN`: Your Bright Data API token for web scraping
- `WEB_UNLOCKER_ZONE`: Bright Data web unlocker zone (default: mcp_unlocker)
- `BROWSER_ZONE`: Bright Data browser zone (default: scraping_browser1)

## Output Features

- **Research Metrics**: View source count, content chunks, total words, and average chunk size
- **Theme Analysis**: See key themes identified with sample insights and source references
- **Generated Content**: Receive markdown-formatted articles or outlines
- **Download Option**: Save generated content as markdown files

## Troubleshooting

- Ensure all API keys are correctly set in the `.env` file
- Check that Node.js and the Bright Data MCP tools are properly installed
- Verify internet connection for web scraping functionality
- Make sure OpenAI API has sufficient credits

## License

This project is for educational and research purposes.
