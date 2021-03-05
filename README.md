# Automatic Terminology Analysis for Data Science Job Descriptions

Project elaborated with Anwesha Tomar and Sandra Valdes Salas. Special thanks to Avijeet Kartikay for offering orientation with web scraping.

This project involves:
Web scraping of Indeed web page.
Extraction of most frequent terminology (unigrams, bigrams, and trigrams) in data science job desriptions.
Comparison between data science terminology and software engineering terminology.
Measure the Tf-idf scores of data science terminology to obtain the most relevant terms.
Analysis of data science terminology found in 6 different U.S. cities (D.C., New York, Chicago, Austin, Los Angeles, San Francsico) and 7 different industries (Healthcare, Banks and financial services, Insurance, Government, Aeropsace and Defense, Technology, Consulting and Business Services).

**Key findings:**

Data Science and Software Engineering job descriptions share common terminology.
Data Science terminology is mostly composed of unigrams and bigrams.
Python, R, Communication skill, Best practice are the most relevant terms in Data Science.
A Chi-squared of independence test concluded that Data Science terminology is dependent upon cities and industries.

**Project files and programs**

Name of the program:  NLP_project_part1_final

Input file: none

Output file: json files

Description: This program consists mainly of the code used for web scraping. After extracting the information, the program creates, as a final output, json files with information about data science and software engineer job descriptions by city. These files were stored in a file called “raw_json_data”.

___________________

Name of the program: NLP_project_part2_final

Input file: json files 

Output file: dataset.csv

Description: This program reads all the json files and transforms them into a dataframe named “dataset.csv”.

___________________

Name of the program: NLP_project_part3_final

Input file: dataset.csv

Intermediate files: df_with_content_zoning (data frame); datascience_complete_terms (data frame); engineer_complete_terms (data frame); EOE.txt; customized_stopwords_for_ngrams.txt

Output file: none (results are presented in the program)

Description: This program consists of the extraction and analysis of terms over the entire data science and software engineer corpora. The processing and analysis is done separately for data science and software engineering. The program: 1) applies content zoning to extract useful paragraphs from the job descriptions; 2) extracts unigrams, bigrams and trigrams for data science and software engineer corpora; 4) calculates the idf score for data science based on a vocabulary of terms. The program uses SpaCy and NLTK for processing the terms.

The program takes as the main input “dataset.csv”. Other files that are required to quickly run this program are the following: 1) a dataframe of all job descriptions with content zoning (“df_with_content_zoning”); 2) a data frame with unigrams of each data science job description (“datascience_complete_terms”); 3) a data frame with unigrams of each software engineer job description (“engineer_complete_terms”); 4) a text file with samples of Equal Opportunity Statements, used for customizing stopwords (“EOE.txt”); 5) a text file with customized stopwords used for extracting ngrams with NLTK (customized_stopwords_for_ngrams.txt).

___________________

Name of the program: NLP_project_part4_final

Input file: datascience_complete_terms (data frame); customized_stopwords_for_ngrams.txt

Output file: none (results are presented in the program)

Description: This program consists of the extraction and analysis of terms of data science job descriptions by 2 dimensions: geography (cities) and industry. The processing and analysis is done separately for “city” and “industry”. The program: 1) extracts unigrams and bigrams for data science segmented by city; 2) extracts unigrams and bigrams for data science segmented by industry. Finally, the program includes Chi2 Test of  Independence for data science terms and cities, and data science terms and industries. 

The program takes as the main input the data frame “datascience_complete_terms”. As a secondary file, the program requires “customized_stopwords_for_ngrams.txt”. 


