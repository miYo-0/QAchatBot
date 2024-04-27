# QAchatBot



# Llama2 QAchatBot

The Llama2 QAchatBot is a powerful tool designed to provide information from the book (A PACT WITH THE SUN Textbook for Class VI) by answering user queries using state-of-the-art language models and vector stores. This README will guide you through the setup and usage of the Llama2 QA Bot.

## Table of Contents

- [Introduction](#QAchatBot)
- [Table of Contents](#table-of-contents)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [License](#license)

## Prerequisites

Before you can start using the Llama2 QAchatBot, make sure you have the following prerequisites installed on your system:

- Python 3.6 or higher
- Required Python packages (you can install them using pip):
    - langchain
    - chainlit
    - sentence-transformers
    - faiss
    - PyPDF2 (for PDF document loading)

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
    ```
    chainlit run model.py -w
    ```

Happy coding with Llama2 QAchatBot! 🚀