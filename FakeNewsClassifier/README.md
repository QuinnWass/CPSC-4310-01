# Fake News Classifier

## Datasets
### Fake News & Real News datasets by Clément Bisaillon
#### fake.csv
* This data set contains text that has been classified as fake. It contains date, media type, title, and text columns
* This file has 21417 rows
* Head and Tail of data
```
[4 rows x 5 columns]
Head of data                                                title  ... classification
0  As U.S. budget fight looms, Republicans flip t...  ...           real
1  U.S. military to accept transgender recruits o...  ...           real
2  Senior U.S. Republican senator: 'Let Mr. Muell...  ...           real
3  FBI Russia probe helped by Australian diplomat...  ...           real
4  Trump wants Postal Service to charge 'much mor...  ...           real

[5 rows x 5 columns]
Tail of data                                                    title  ... classification
21412  'Fully committed' NATO backs new U.S. approach...  ...           real
21413  LexisNexis withdrew two products from Chinese ...  ...           real
21414  Minsk cultural hub becomes haven from authorities  ...           real
21415  Vatican upbeat on possibility of Pope Francis ...  ...           real
21416  Indonesia to buy $1.14 billion worth of Russia...  ...           real
```
* Columns: title, text, and subject are all strings. date is a date type. Title and text are the main data points for this dataset. They contain raw data from articles or other mediums
```
Column names: Index(['title', 'text', 'subject', 'date'], dtype='object')
```
* Measures of central tendancy: It is difficult to quanitfy anyhting about this dataset without proccessing


#### real.csv
* The real dataset is of the same form as the fake dataset
* This dataset has 21417 rows
```
4 rows x 5 columns]
Head of data                                                title
0  As U.S. budget fight looms, Republicans flip t...  ...           real
1  U.S. military to accept transgender recruits o...  ...           real
2  Senior U.S. Republican senator: 'Let Mr. Muell...  ...           real
3  FBI Russia probe helped by Australian diplomat...  ...           real
4  Trump wants Postal Service to charge 'much mor...  ...           real

[5 rows x 5 columns]
Tail of data                                                    title  
21412  'Fully committed' NATO backs new U.S. approach...  ...           real
21413  LexisNexis withdrew two products from Chinese ...  ...           real
21414  Minsk cultural hub becomes haven from authorities  ...           real
21415  Vatican upbeat on possibility of Pope Francis ...  ...           real
21416  Indonesia to buy $1.14 billion worth of Russia...  ...           real
```

## Data Preprocessing
To preprocess the data we took an NLP specific approach. We removed stop words since they do not carry relevence, and constrained our data to only alphabetical data. Additionally, we lemmatized the data. 

After that we calculated the sentiment using NLTK for each text and title element and stored it on the row. Following this, we counted the parts of speech for each row using NTLK.

## Exploratory data analysis


## Preliminary data analysis report 
We found that while both fake and real news have faily balanced sentiments, the fake news had a slighly negative mean and the real news had a slightly positive mean.

Additionally, while the general clustering of word counts was similar in fake news and real news, fake news had a significant number of outliers. 

Graphs for this data can be found in our notebook.
