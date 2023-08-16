# Natural Language Toolkit (NLTK) Chatbot - Retrieval Learning

Welcome to the NLTK Chatbot GitHub repository! 🤖

This repository contains code for a retrieval-based chatbot built using Python's NLTK library. The chatbot leverages a TF-IDF (Term Frequency-Inverse Document Frequency) approach to match user questions with the most suitable sentences from its knowledge base. The knowledge base is sourced from a `data.txt` file and focuses on providing information about the universe from Wikipedia.

## Features

- **Retrieval Learning:** The chatbot uses a retrieval learning approach to find the most relevant response to user queries based on the sentences stored in the `data.txt` file.

- **Preprocessing:** Text preprocessing is performed using NLTK's `punkt` tokenizer and WordNet lemmatization. This ensures that user input and sentences in the knowledge base are processed consistently.

- **Greeting Responses:** The chatbot responds to greetings with various friendly responses. It recognizes common greetings and provides appropriate replies.

## How to Use

1. Clone the repository to your local machine.
   
   git clone https://github.com/sanjay-k-j/chat_bot_using_nltk.git


2. Install the required libraries: `numpy`, `nltk`, `sklearn`, and `random`.

3. Update `data.txt`: Fill this file with sentences containing information about the universe. Each sentence should be on a new line.

4. Run `chatbot.py`: Execute the script to start the chatbot. You can interact with the bot by inputting text queries.

5. Continuous Conversation: The chatbot can engage in a continuous conversation. After receiving the bot's response, you can provide further input to continue the conversation.

## Files and Functions

- `chatbot.py`: Main script to run the chatbot.
- `preprocessing.py`: Contains functions for text preprocessing and greeting responses.
- `data.txt`: Knowledge base sentences about the universe.

## Emoji Key

- 🤖: Chatbot
- 👋: Greeting
- 🌌: Universe Information
- 🔍: Retrieval Learning
- 📚: Knowledge Base

Feel free to contribute by improving the code, adding more functionality, or enhancing the chatbot's responses! Happy coding! 😊🚀

