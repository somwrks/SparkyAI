# SparkyAI

A Discord bot that uses RAG (Retrieval-Augmented Generation) via web scraping to provide specific answers about Arizona State University.

https://github.com/user-attachments/assets/1c380302-7fb4-4025-acfc-09840b42017d

## Description:
    
This Discord bot uses the LangChain library to create a question-answering system.
It uses the Hugging Face Hub to download pre-trained models and embeddings,
and integrates with the Qdrant vector database for efficient search.
The bot also supports multi-step reasoning, allowing users to ask questions
that require multiple pieces of information from different sources. It also lists the citations used for the information

The bot also supports natural language inference (NLI) using the
Google Generative AI model. To use NLI, you must provide a
question and two options, and the bot will generate a third option
that is most likely to be the correct answer.

The current use for this bot is to provide answers to questions regarding arizona state university 

## Technical Workflow

![Untitled-2024-06-20-0039](https://github.com/user-attachments/assets/7df755a4-fc82-4d48-8a47-b573f36de33f)


- The bot starts by connecting to the Qdrant vector database.
- It then retrieves relevant documents from the database using the ASU University's search terms.
- The bot uses the Hugging Face pipeline to generate answers based on the retrieved documents.
- If a user asks a question that requires multi-step reasoning, the bot will generate a series of answers, each based on the previous one.
- To handle natural language inference (NLI), the bot uses the Google Generative AI model.
- The bot is designed to handle a variety of questions related to ASU University, such as academic information, campus life, and student life.


## Features

![{7F674D52-3D85-48C9-9EF4-9D7DD2BFF9AA}](https://github.com/user-attachments/assets/7b1e0966-cd73-4779-b928-6850358d93ad)
![image](https://github.com/user-attachments/assets/b81a4c26-e32d-43b3-b360-f4bbbb7847a7)
![image](https://github.com/user-attachments/assets/b1bdb741-20ee-4619-9cff-8ea728e696bb)
![image](https://github.com/user-attachments/assets/b122836a-c9c3-46e3-a5bd-f3369b73778e)


- Uses LangChain library for question-answering capabilities
- Integrates with Hugging Face Hub for pre-trained models and embeddings
- Leverages Qdrant vector database for efficient search
- Supports multi-step reasoning for complex queries
- Provides citations for information sources
- Includes natural language inference using Google Generative AI
- Specializes in answering questions about Arizona State University

## Technical Stack

- LangChain for RAG implementation
- Hugging Face Hub integration
- Qdrant vector database
- Google Generative AI for NLI
- Discord.py for bot functionality
- BeautifulSoup for WebScraping along with Google Search Engine

## Setup

1. Clone the repository
2. Install required dependencies
3. Configure environment variables
4. Run the bot using the provided Jupyter notebook
5. Run Qdrant vector server `docker run -p 6333:6333 qdrant/qdrant`

## Usage

The bot can be used in Discord servers to:
- Answer questions about ASU
- Provide multi-step reasoning for complex queries
- Generate natural language inferences
- Cite sources for provided information

## Current Todos-

- [x]  setup langchain technologies
- [x]  develop and refine strict prompt template
- [x]  experiment with different models
- [x]  test
- [x]  setup discord bot
- [x]  convert code to discord bot
- [x]  host on replit
- [x]  test
- [x]  stop initializing vector db every instance
- [x]  create action functions and followup functions for bot to integrate the server
- [x]  test differnet models
- [x]  improve speed
- [x]  have better logging in backend
- [ ]  implement dynamic search
- [ ]  keyword-channel search in discord for question
- [ ]  display the ongoing actions by llm to response
- [ ]  add asurite verification feature with faceid
- [ ]  data analystics board on website- request questions, steps of llm, responses, time, frequency
- [ ]  safety feature- track or identify heated argument, formal warning in dms of people
- [ ]  final testing
- [ ]  research hosting services


### Custom GenAI Module Edit

I edited the gemini module files for implementing asynchronous functions as the tools for the gemini agents when working in a connected environment of connected gemini agents.

You can use asynchronous functions as tools for gemini agents by editing the `venv\Lib\site-packages\google\generativeai\types\content_types.py`  with `custom_module_files/content_types.py`



