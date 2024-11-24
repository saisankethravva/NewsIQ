
# NewsIQ: News Research Tool 

NewsIQ is a user-friendly news research tool designed for effortless information retrieval. Users can input article URLs and ask questions to receive relevant insights from the stock market and financial domain.


## Features

- Load URLs or upload text files containing URLs to fetch article content.
- Process article content through LangChain's UnstructuredURL Loader
- Construct an embedding vector using OpenAI's embeddings and leverage FAISS, a powerful similarity search library, to enable swift and effective retrieval of relevant information
- Interact with the LLM's (Chatgpt) by inputting queries and receiving answers along with source URLs.


## Installation

1.Clone this repository to your local machine using:

```bash
  git clone https://github.com/saisankethravva/NewsIQ.git
```
2.Navigate to the project directory

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
streamlit run main.py

```

2.The web app will open in your browser.

- On the sidebar, you can input URLs directly.

- Initiate the data loading and processing by clicking "Process URLs."

- Observe the system as it performs text splitting, generates embedding vectors, and efficiently indexes them using FAISS.

- The embeddings will be stored and indexed using FAISS, enhancing retrieval speed.

- The FAISS index will be saved in a local file path in pickle format for future use.
- One can now ask a question and get the answer based on those news articles
- Sample news articles
  - https://www.cnbc.com/2024/11/20/nvidia-nvda-earnings-report-q3-2025.html
  - https://nvidianews.nvidia.com/news/nvidia-announces-financial-results-for-third-quarter-fiscal-2025
  - https://www.livemint.com/market/stock-market-news/nvidia-q3-result-stock-declines-even-as-revenue-nearly-doubles-guidance-fails-to-meet-expectations-11732149987999.html

## Project Structure

- main.py: The main Streamlit application script.
- requirements.txt: A list of required Python packages for the project.
- faiss_store_openai.pkl: A pickle file to store the FAISS index.
- .env: Configuration file for storing your OpenAI API key.


## Why I did this project

Stock investing requires staying informed about market trends, company performance, and financial news. Managing a portfolio of 50 stocks with a total value of $30,000 presents the challenge of continuously tracking quarterly reports, company news, and market insights. Over time, this manual process became increasingly tedious and time-consuming.

To address this, I developed NewsIQ, a user-friendly news research tool that simplifies information retrieval for stock market enthusiasts and investors. The purpose of this project was to streamline the process of analyzing stock-related news and quarterly reports, making it more efficient and accessible. By allowing users to input article URLs and ask questions, NewsIQ provides relevant insights from the financial domain, helping users stay informed without the need to sift through overwhelming amounts of information.

This project reflects my commitment to leveraging technology for personal finance management and creating tools that enhance decision-making in stock investing. NewsIQ bridges the gap between raw financial data and actionable insights, making it easier to stay updated and make informed investment choices.


## Future Enhancements.

NewsIQ is currently a proof of concept for a comprehensive project that aims to revolutionize how investors access and interpret financial news. While the current iteration demonstrates the potential of retrieving insights from article URLs, future plans focus on building a robust data ingestion system. This system will include a web scraper powered by Bright Data, capable of scanning major financial news platforms like The Economic Times, Wall Street Journal, Bloomberg, CNBC, and Investopedia on a scheduled basis using cron jobs.

The scraped articles will be processed to generate embeddings and stored in a vector database, enabling efficient retrieval of contextually relevant information. To enhance usability, I plan to develop an intuitive user interface using React, featuring chat capabilities that interact with the vector database. This setup will allow users to query the database, retrieve similar chunks of data, and get precise, actionable insights.

This project reflects my passion for combining cutting-edge technology with financial analysis to streamline stock market research, enabling better-informed investment decisions.

## Likes

1. Time-Saving: Automates the tedious process of gathering and summarizing financial information, allowing investors to focus on decision-making.
2. Educational Value: Offers an opportunity to work with advanced tools like Bright Data, embeddings, and vector databases, providing learning and development potential.


## Dislikes:
1. Dependency on External APIs: Reliance on financial news websites and Bright Data may introduce challenges like API rate limits, scraping restrictions, or data availability.
2. High Maintenance: Requires regular updates to the scraper and embedding algorithms to adapt to changes in website structures and news patterns.


## Sample images of Working model


![Screenshot 2024-11-24 at 4 40 44 PM](https://github.com/user-attachments/assets/b1ee3f91-3ae2-4296-83e8-54ed1e8a8e4e)



![Screenshot 2024-11-24 at 4 40 01 PM](https://github.com/user-attachments/assets/2d45046d-a84d-42b8-8b29-a64e8cfbde06)


![Screenshot 2024-11-24 at 4 39 02 PM](https://github.com/user-attachments/assets/32808a9d-17ab-4be4-856c-d877ed48ea40)




