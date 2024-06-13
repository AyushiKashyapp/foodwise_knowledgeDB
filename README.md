# Food Wise and Food Vision Knowledge DB
A knowledge database created on neo4j using triples extracted by roberta llm and named entity recognition. 

# Project Motivation
Adding the Food Wise 2025 and Food Vision 2030, two strategies by Ireland's Department of Agriculture, Food and Marine, to implement sustainable food systems (SFS) on the global stage. I aim to extract the major stakeholders from official project plan documents and manually find the important people at authority and committee members, and create a knowledge database with their wikipedia pages or any online information pages in neo4j.

# File ExtractStakeholders.ipynb: Extracting major Food Wise and Food Vision Stakeholders

# Aim:

The aim is to extract major ***stakeholder organisations*** involved in the Food Wise 2025 and Food Vision 2030 projects. 

The stakeholders are extracted from the official documentation files and implementation plans available at the Gov.ie website. The ***stakeholders*** are identified as the ***organisations*** mentioned in these documentations.

This code explains how to extract organization names from PDF documents using a RoBERTa-based Named Entity Recognition (NER) model and save them into an Excel file to support structured data storage and reusability. The code will use the files available in source_doc folder, utilize them to extract stakeholder names and output them as a stakeholder.xlsx file to be later utilised for knowledge database creation.
