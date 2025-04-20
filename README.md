# 🍽️ Zomato RAG Chatbot

This is an end-to-end **Generative AI solution** that uses **web scraping** and **Retrieval-Augmented Generation (RAG)** to help users ask natural language questions about restaurants in **Kanpur** and receive contextual, accurate answers.

---

## Features

- Scrapes real restaurant data from Zomato (using Selenium + BeautifulSoup)
- Creates a searchable vector database using Sentence Transformers
- Uses a RAG-based pipeline with Groq API (LLaMA3) for answering queries
- Supports queries like:
  - *"Which restaurant has vegetarian options?"*
  - *"Compare the prices between Restaurant A and B"*

---
## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/zomato-rag-chatbot.git
cd zomato-rag-chatbot
###2. Dependencies include:

selenium

beautifulsoup4

pandas

sentence-transformers

groq

numpy

streamlit or gradio (if UI is used)

###3. Scrape Restaurant Data
Update the list of Zomato URLs in test_zomato_scrapper.py, then run:

bash
Copy
Edit
python test_zomato_scrapper.py
This will generate a restaurant_data.csv file in the data/ directory.

Run the Chatbot
bash
Copy
Edit
python app.py
Alternatively, if using Streamlit:

bash
Copy
Edit
streamlit run app.py
Project Structure
bash
Copy
Edit

### Configuration
Edit src/config.py to adjust:

Path to the dataset (CSV_PATH)

Embedding model (EMBEDDING_MODEL)

LLM behavior and rules (SYSTEM_PROMPT)

### Limitations
The chatbot only responds based on the scraped context.

Questions outside this domain will return "I don't know" responses.

Live data scraping may be subject to Zomato's site changes and policies.
