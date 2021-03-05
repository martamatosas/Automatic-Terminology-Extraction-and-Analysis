# Automatic-Job-Description-Terminology-Analysis

Unsupervised natural language processing model to extract data science and software engineering job descriptions terminology to identify and compare skill requirements by location and industry

BRIEF DESCRIPTION:

The data was Web scraped of Indeed web page.

Extraction of ngrams from the job descriptions.

Comparing data science and software engineering terminology.

Calculated the tf-idf scores to obtain the most relevant data science terms.

Extraction of data science terminology in 6 different U.S. cities and 7 different industries.

The chi-squared of independence between data science terminology, cities and industries was calculated.

**Project files and programs

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


