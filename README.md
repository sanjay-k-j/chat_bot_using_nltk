Creating a Natural language toolkit chatbot using python.

This is a Retrival learning chatbot.

import libraries Numpy, nltk, string, sklearn and random.

this chat gives information about universe present in wekipedia that is stored in .

we are using punkit tokenizer(to understand the human chat formats in different ways) and wordnet dictionary.

we convert data.txt into words and sentences and we stores it in the form of lists in word_token and sentence token.

Lemmatize these tokens

create a resonses to greetings

lemmer: This is an instance of the WordNet Lemmatizer from the NLTK library. Lemmatization is the process of reducing words to their base or root forms. This object is used within the LemTokens function.

LemTokens(tokens): This function takes a list of tokens (words) as input and returns a list of lemmatized tokens using the lemmer instance. It applies lemmatization to each token in the input list.

remove_punc_dict: This dictionary is used to remove punctuation from text. It maps each punctuation character to None in order to eliminate them from the text.

LemNormalize(text): This function is the main preprocessing function. It takes a text input, converts it to lowercase, removes punctuation using the remove_punc_dict, tokenizes the text into words using NLTK's word_tokenize, and then lemmatizes the tokens using the LemTokens function.

greet_inputs: This is a tuple containing various greeting phrases like 'hello', 'hi', 'whassup', and 'how are you?'.

greet_responses: This is a tuple containing corresponding responses like 'hi', 'Hey', 'Hey There!', and 'Hello mate!!'.

greet(sentence): This function takes a sentence (string) as input.

Inside the function, the input sentence is split into individual words using sentence.split().

The function then iterates through each word in the split sentence.

If a lowercase version of the current word matches any of the words in greet_inputs, the function randomly selects and returns a response from greet_responses.

TfidfVectorizer is initialized with a custom tokenizer function LemNormalize and English stopwords are removed.

tfidf is calculated for the predefined set of "sentence_tokens" using the TF-IDF vectorizer.

Cosine similarity is calculated between the TF-IDF representation of the user's input and all the sentences in the "tfidf" matrix.

The index of the most similar sentence (excluding the user's input itself) is determined from the cosine_similarity result.

The "flat" array is sorted, and the second-to-last value is stored as req_tfidf.

If req_tfidf is 0, it indicates no similarity was found, and the bot responds with an "Unable to understand you!" message.

Otherwise, the bot's response is set to the sentence corresponding to the index determined earlier.

However, there are a couple of things to consider:

The code snippet references a function LemNormalize and variable sentence_tokens which are not provided here. You would need to ensure that LemNormalize is a function that performs lemmatization and normalization on input text, and sentence_tokens contains the sentences you're comparing the user input against.

The code assumes that the variable user_response contains the user's input.

Depending on how sentence_tokens is created and the nature of the input data, you might need to preprocess the text further to ensure accurate results.

Consider handling cases where req_tfidf might not be exactly 0 but still very low. This could be done by setting a threshold below which the bot would respond with something like "I'm not sure what you mean."

If you're using this code in a larger system, make sure that the necessary libraries (TfidfVectorizer, cosine_similarity, etc.) are imported properly.

Remember to provide a proper mechanism for the bot to engage in a continuous conversation by calling this function iteratively with user responses








