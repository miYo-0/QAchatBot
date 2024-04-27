# Chat Bot Project README

This project implements a chat bot that utilizes language models and retrieval-based question answering techniques to interactively respond to user queries. The project is structured into two main files: `main.py` and `model.py`.

## Table of Contents

- [Introduction](#QAchatBot)
- [Table of Contents](#table-of-contents)
- [Files](#Files)
- [Dependencies](#Dependencies)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [License](#license)

## Files
1. `main.py` This file contains code for creating the vector database from PDF documents in a specified directory.
   * create_vector_db(): Function to create the vector database by loading PDF documents, splitting text, generating embeddings, and saving the database locally using FAISS.
2. `model.py` This file contains code for the question-answering model and chat bot interaction logic.
  * `set_custom_prompt()`: Function to define a custom prompt template for the QA retrieval process.
  * `retrieval_qa_chain(llm, prompt, db)`: Function to create a retrieval-based question answering chain using the specified language model, prompt template, and vector database.
  * `load_llm()`: Function to load the language model for question answering.
  * `qa_bot()`: Function to initialize the question-answering bot by loading the vector database, language model, and prompt template.
  * `final_result(query)`: Function to obtain the final response from the chat bot for a given user query.
  * `@cl.on_chat_start` and `@cl.on_message`: Decorators to define the behavior of the chat bot when a conversation starts and when a message is received, respectively.


## Prerequisites

Before you can start using the Llama2 QAchatBot, make sure you have the following prerequisites installed on your system:

- Python 3.6 or higher
- Required Python packages (you can install them using pip):
    - langchain
    - chainlit
    - sentence-transformers
    - faiss
    - PyPDF2 (for PDF document loading)
 
## Dependencies
* `langchain_community`: A library for language processing tasks, including embeddings, vector stores, document loaders, and LLMS.
* `chainlit`: A library for building conversational AI models with chaining logic.

## Installation

1. Clone this repository to your local machine.

    ```bash
    git clone https://github.com/your-username/QAchatBot.git
    cd QAchatBot
    ```

2. Create a Python virtual environment (optional but recommended):

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use: venv\Scripts\activate
    ```

3. Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

4. Download the required language models and data. Please refer to the Langchain documentation for specific instructions on how to download and set up the language model and vector store.

5. Set up the necessary paths and configurations in your project, including the `DB_FAISS_PATH` variable and other configurations as per your needs.

## Getting Started

To get started with the Llama2 QAchatBot, you need to:

1. Set up your environment and install the required packages as described in the Installation section.

2. Configure your project by updating the `DB_FAISS_PATH` variable and any other custom configurations in the code.

3. Prepare the language model and data as per the Langchain documentation.

4. Start the bot by running the provided Python script or integrating it into your application.

## Usage

The Llama2 QAchatBot can be used for answering queries related to aforementioned book. To use the bot, you can follow these steps:

1. Start the bot by running your application or using the provided Python script.

2. Send a query to the bot.

3. The bot will provide a response based on the information available in its database.

4. If sources are found, they will be provided alongside the answer.

5. The bot can be customized to return specific information based on the query and context provided.


## License

This project is licensed under the MIT License.

---

For more information on how to use, configure, and extend the Llama2 QAchatBot, please refer to the Langchain documentation or contact the project maintainers.

## For my personal reference
    ```bash
    chainlit run model.py -w
    ```

Happy coding with Llama2 QAchatBot! 🚀
