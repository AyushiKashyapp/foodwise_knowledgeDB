# Project Question Bank

1. **What is the purpose of the transformers library in this context?**
   Hugging Face Transformers is an open-source framework for deep learning created by Hugging Face. It provides APIs and tools to download state-of-the-art pre-trained models and further tune them to maximize performance. These models support common tasks in different modalities, such as natural language processing, computer vision, audio, and multi-modal applications. The transformers library is used to load and use the RoBERTa-based Named Entity Recognition (NER) model to identify and extract organization names from the text extracted from the PDFs.

2. **Explain the role of pdfminer.six in this project.**
  Pdfminer.six is a python package for extracting information from PDF documents. Parse all objects from a PDF document into Python objects. Analyze and group text in a human-readable way. The pdfminer.six library is used to extract text content from PDF documents, which is necessary before performing Named Entity Recognition (NER) to identify organizations.

3. **Why do we need to install the en_core_web_sm model from spacy?**
   en_core_web_sm is a small English pipeline trained on written web text (blogs, news, comments), that includes vocabulary, syntax and entities. It is used for additional text processing and potentially enhancing the NER capabilities by providing a pre-trained language model for the English language.

4. **What are the steps involved in extracting and saving the organization names?**
   The steps involved are:

- Extract text from PDF documents using pdfminer.six.
- Use the RoBERTa-based NER model from the transformers library to identify and extract organization names from the text.
- Process the extracted names using spacy for any additional text processing.
- Save the extracted organization names into an Excel file using pandas.

5. **What libraries are required to run the triple extraction?**
- transformers for natural language processing tasks.
- wikipedia to access and parse data from Wikipedia.
- newspaper3k for extracting and parsing articles from websites.
- pyvis for visualization of graphs and networks.
- pandas for handling dataframes and Excel files.
- IPython for interactive computing.
- GoogleNews for fetching news articles.

6. **What does the wikipedia library do in this project?**
The wikipedia library is used to access and parse data from Wikipedia pages about the stakeholders and committee members of the projects.

7. **How are the URLs for the stakeholder organizations and committee members read into the code?**
The URLs are read from an Excel file named stakeholders.xlsx using the pandas library and stored in a list called urls.

8: **What is the purpose of the extract_relations_from_model_output function?**
The purpose of the extract_relations_from_model_output function is to process the text output from the model and extract relationships (triples) by identifying the subject, relation, and object from the text.

9. **What does the KB class do in the code?**
The KB (Knowledge Base) class manages relations by providing methods to add, merge, and print them. It helps in organizing the extracted relations into a structured format.

10. **Explain the role of the from_text_to_kb function.**
The from_text_to_kb function tokenizes the input text into spans, generates relations using the rebel-large model, and organizes them into a knowledge base (KB) object.

11. **What is the purpose of the article_extraction function?**
The article_extraction function extracts and concatenates text from multiple articles using the newspaper library, which is then used for relation extraction.

12. **How is text cleaning performed in this code?**
Text cleaning is performed using the clean_text function, which removes special characters, emojis, and any other unwanted characters from the text.

13. **Why is it necessary to split the text into smaller chunks?**
It is necessary to split the text into smaller chunks because the rebel-large model cannot process texts over 1029 tokens. The create_chunks function is used to split the text into manageable chunks.

14. **How is the knowledge base (KB) created from text chunks?**
The knowledge base (KB) is created from text chunks using the create_kb_from_text_chunks function, which iterates over the chunks, extracts relations from each chunk, and stores them in a dictionary.

15. **How are the extracted relations stored in a dataframe?**
The extracted relations are stored in a dataframe where each row corresponds to a chunk of text and contains the relations' dictionaries. This dataframe is then flattened to store each part of the relation (head, type, and tail) as separate columns in a new dataframe.

16. **How is the rebel-large model loaded into the code?**
The rebel-large model is loaded using the AutoModelForSeq2SeqLM and AutoTokenizer classes from the transformers library. REBEL is a seq2seq model based on BART that performs end-to-end relation extraction for more than 200 different relation types.

17. **Give overview of RoBERTa.**
RoBERTa (short for “Robustly Optimized BERT Approach”) is a variant of the BERT (Bidirectional Encoder Representations from Transformers) model. Like BERT, RoBERTa is a transformer-based language model that uses self-attention to process input sequences and generate contextualized representations of words in a sentence.
