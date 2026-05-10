# Research_mind
A simple multi-agent research system built with LangChain, Tavily, BeautifulSoup, and Streamlit.

## Overview

ScoutAI takes a research topic, searches the web for relevant information, reads deeper content from selected sources, writes a draft report, and then critiques the report to improve quality.

## Features

- Search agent for finding recent and relevant web information
- Reader agent for scraping deeper content from selected URLs
- Writer chain for generating a research report
- Critic chain for reviewing the final report
- Streamlit UI for running the pipeline interactively

## Project Flow

1. User enters a research topic
2. Search agent gathers relevant search results
3. Reader agent selects and scrapes a useful source
4. Writer chain drafts the report using collected research
5. Critic chain reviews the draft and gives feedback

## Tech Stack

- Python
- LangChain
- Tavily API
- BeautifulSoup
- Streamlit
- Mistral API / OpenAI-compatible setup
- Hugging Face

## Project Structure

```bash
multiAgent_system/
│── app.py
│── pipeline.py
│── agents.py
│── tools.py
│── requirements.txt
│── .env
```

## Installation

```bash
git clone <your-repo-url>
cd multiAgent_system
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

## Environment Variables

Create a `.env` file in the project root:

```env
TAVILY_API_KEY=your_tavily_api_key
MISTRAL_API_KEY=your_mistral_api_key
OPENAI_API_KEY=your_openai_api_key
HF_TOKEN=your_huggingface_token
```

## Run the Streamlit App

```bash
streamlit run app.py
```

## Example Usage

- Enter a topic such as `Impact of AI on Data Engineering`
- Run the pipeline
- Review search results, scraped content, final report, and critic feedback in the UI

## Notes

- If Tavily import fails, install `tavily-python`
- If `torch` is missing, install PyTorch dependencies
- If using `ChatOpenAI`, make sure `OPENAI_API_KEY` is set
- If Hugging Face returns a 402 error, billing or credits may be exhausted

## Future Improvements

- Add memory support
- Add downloadable report export
- Add multiple source scraping
- Add model/provider selection from the UI
- Add better error handling and logging
