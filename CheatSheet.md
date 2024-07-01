# Project Cheatsheet

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
