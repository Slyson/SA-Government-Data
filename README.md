# South African Presidential Statements Dataset
### I cannot upload the dataset to github, unfortunately, but it can be acccessed from <a href="https://www.kaggle.com/datasets/maleselalegodi/sa-government-data/data"> my kaggle account </a>
## Overview
This dataset contains South African presidential statements translated into multiple South African languages. It is a valuable resource for tasks in **Natural Language Processing (NLP)** and **Machine Translation**, particularly for low-resource languages. Multilingual datasets for South African languages are scarce, making it challenging to build robust NLP models. This dataset helps fill that gap by providing presidential statements in multiple South African languages. This datasets contains statements from 9 February until 9 October 2023. This is my contribution, hopefully this is helpful.

### Folders and files in the Dataset
1. **Unorganised Datasets (folder):`presidential_statements.json`(file)**:
    - Contains presidential statements drafted in South African languages.
   
2. **Organised Datasets (folder):`nso_xh_ts.json`(file)**:
    - Contains translations of the presidential statements these three languages:
      - **Northern Sotho (NSO)**
      - **isiXhosa (XH)**
      - **Xitsonga (TS)**

3. **Notes (folder):`statements_urls.txt`(file) and `unbalanced_statements_data_info.txt`(file)**:
    - Contains files which describe the nature of the data
      - **`statements_urls.txt`** is file with the list of urls from which the statements were extracted.
      - **`unbalanced_statements_data_info.txt`** is a file with statements which do not have 10 translations
       
4. **Scripts (folder): `multilingual-statement-scraping.ipynb` (file) and `link-scraping.ipynb` (file)**
    - **link-scraping.ipynb** This script scans pages on the South African Presidency's website to identify URLs that contain multilingual translations of presidential statements. It checks for accessible translation pages and saves the valid URLs to a text file.
    - **`multilingual-statement-scraping.ipynb`** This script scrapes multilingual presidential statements from a series of web pages and identifies and processes language-specific links on each page, extracts the corresponding text of the statements, and then organises the data into a structured dictionary.

### Applications
There are many, but the structure is perfect for
     1. **Machine Transaltion:** Build and evaluate models for translating between all spoken South African languages.
     2. **Low-Resource NLP Research:** Enhance language understanding for underrepresented and under-resourced languages.
     3. **Sentiment Analysis:** Analyse public sentiments in different languages using presidential speeches.    
    
### Dataset Structure
Each file is structured as a JSON object with keys representing unique statement IDs. The translations are aligned across languages to facilitate easy use in NLP tasks.

### Example JSON Structure
```JSON
{
    Statement 1": {
            "Afrikaans" : { "link" : url
                            "statement" : text
                }
            "English(source)" : { "link" : url
                            "statement" : text
                }
            "isiNdebele" : { "link" : url
                            "statement" : text
                }
            "isiXhosa" : { "link" : url
                            "statement" : text
                }
    }
}
