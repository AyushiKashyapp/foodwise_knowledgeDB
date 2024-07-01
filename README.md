# Food Wise and Food Vision Knowledge DB
A knowledge database created on neo4j using triples extracted by roberta llm and named entity recognition. 

Find the project question bank here [QuestionBank](https://github.com/AyushiKashyapp/foodwise_knowledgeDB/blob/main/QuestionBank.md)

# Project Motivation
Adding the Food Wise 2025 and Food Vision 2030, two strategies by Ireland's Department of Agriculture, Food and Marine, to implement sustainable food systems (SFS) on the global stage. I aim to extract the major stakeholders from official project plan documents and manually find the important people at authority and committee members, and create a knowledge database with their wikipedia pages or any online information pages in neo4j.

# File ExtractStakeholders.ipynb: Extracting major Food Wise and Food Vision Stakeholders.

Aim:
The aim is to extract major ***stakeholder organisations*** involved in the Food Wise 2025 and Food Vision 2030 projects. 

The stakeholders are extracted from the official documentation files and implementation plans available at the Gov.ie website. The ***stakeholders*** are identified as the ***organisations*** mentioned in these documentations.

This code explains how to extract organization names from PDF documents using a RoBERTa-based Named Entity Recognition (NER) model and save them into an Excel file to support structured data storage and reusability. The code will use the files available in source_doc folder, utilize them to extract stakeholder names and output them as a stakeholder.xlsx file to be later utilised for knowledge database creation.

# File TripleExtraction.ipynb: Extracting relations from web pages.

Aim:
The aim is to extract relations (triples) from wikipedia and other online information pages available for major stakeholders and committee members of Food Wise 2025 and Food Vision 2030 projects.

The code overall follows these major steps:

Get the URLs for the stakeholder organisations and committee members from an excel.
Scrape the webpages and store the scrapped data in the form of a string to be tokenized.
Extract the entities and relations from the graph using rebel-large model.
Export the extracted relations to an excel.

# Extracted Excel Files: stakeholders and triples_data

Extracted excel file from ExtractStakeholder.ipynb containing data for stakeholders (Names and web page links).
Extracted excel file from TripleExtraction.ipynb containing data for extracted relations (triples - head, type and tail).

# File Neo4jGraphCreation.ipynb: Generating a knowledge graph in Neo4j.

Generating a Neo4j Knowledge Graph using the extracted triples.
A knowledge graph created using the triples extracted in the previous parts of the project, sources from the wikipedia pages and web pages of the major stakeholders and committess members of the Food Wise and Food Vision projects.

# File VisualiseKG.ipynb: Visualising the generated knowledge graph.

Visualising Knowledge Graph using pyvis.network by reading the triples extracted in previous steps of the project.

The graph is later exported as an HTML file named: "foodwise_and_foodvision.html"

# Graph Snippet

![image](https://github.com/AyushiKashyapp/foodwise_knowledgeDB/assets/147310638/df5a4802-5f74-47d5-866f-b8bcaf232fb1)
