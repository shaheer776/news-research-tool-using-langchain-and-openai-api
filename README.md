# News Research Tool Using Langchain and OpenAI API
This user-friendly news research tool is designed for effortless information retrieval. Users can input article URLs and ask questions to receive relevant insights from the provided blogs and news articles. The model outputs relevant answer to the query as well the source through which it was able to fetch that answer.

<img width="2560" height="1240" alt="news_research_tool" src="https://github.com/user-attachments/assets/882056d6-44ee-4706-a9d9-87a600104f5e" />


## Features

- Load URLs or upload text files containing URLs to fetch article content.
- Process article content through LangChain's UnstructuredURL Loader
- Construct an embedding vector using OpenAI's embeddings and leverage FAISS, a powerful similarity search library, to enable swift and effective retrieval of relevant information
- Interact with the LLM's (Chatgpt) by inputting queries and receiving answers along with source URLs.


## Installation

1.Clone this repository to your local machine using:

```bash
  git clone [Github Link](https://github.com/shaheer776/news-research-tool-using-langchain-and-openai-api.git)
```
2.Navigate to the project directory:

```bash
  cd 2_news_research_tool_project
```
3. Install the required dependencies using pip:

```bash
  pip install -r requirements.txt
```
4.Set up your OpenAI API key by creating a .env file in the project root and adding your API

```bash
  OPENAI_API_KEY=your_api_key_here
```
## Usage/Examples

1. Run the Streamlit app by executing:
```bash
streamlit run news_research_tool.py

```

2.The web app will open in your browser.

- On the sidebar, you can input URLs directly.

- Initiate the data loading and processing by clicking "Process URLs."

- Observe the system as it performs text splitting, generates embedding vectors, and efficiently indexes them using FAISS.

- The embeddings will be stored and indexed using FAISS, enhancing retrieval speed.

- The FAISS index will be saved in a local file path in pickle format for future use.
- One can now ask a question and get the answer based on those news articles
- In the image, we used following news articles
  - [Link-1](https://www.marketpulse.com/markets/golds-xauusd-price-forecast-mixed-signals-ahead-of-nfp-a-return-above-3300oz-or-further-downside-ahead/)
  - [Link-2](https://www.dailyforex.com/forex-technical-analysis/2025/07/gold-forecast-18-july-2025/231399)
  - [Link-3](https://timesofindia.indiatimes.com/business/india-business/gold-price-prediction-today-where-are-gold-rates-headed-on-august-05-2025-and-in-the-near-term-mcx-gold-outlook/articleshow/123111129.cms)

## Project Structure

- news_research_tool.py: The main Streamlit application script.
- requirements.txt: A list of required Python packages for the project.
- .env: Configuration file for storing your OpenAI API key.
