# Text-Summarization-NLP

This is a basic python project in which we have done summarization of data in region language i.e Hindi.
## Method 
### Read the input file
### Pre-processing the data
- Sentence Segmentation -  In Hindi, sentence is segmented by identifying boundary of sentence that ends with (|).
- Tokenization of each sentence to words - Breaking the sentence into dicrete tokens.
- Stop Words Removal - Removing words that carry less importance then the keywords.
- Stemming of Words - Removing the suffix to get the common origin.

### Processing Step (feature extraction + sentence ranking)
1. Extract following features from text file
- Average TF-ISF - To evaluate how imoortant the word is in the document
- Sentence length - Removing the sentence which are too short or too long by providing upper and lower bounds.
- Sentence Position - To determine how many sentences in the beginning and at the end are retained in summary.
- Sentence Similarity - To determine similarity between two sentences.
- Numerical Data - Sometimes numeric data is important eg. DOB, stats, important dates etc. 
2. Sentence ranking to rank sentences in range of '0 to 1' with 1 indicating most important
and 0 indicating not important sentence based on the each feature’s normalized scores.
### Generate Summary
While (Sentences in Summary file does not exceed maximum limit as per given by compression
ratio) extract all sentences from the file sort by sentence rank of Maximum rank (rank5) to
minimum (rank1).

### Conclusion
There is no proper way to determine if the summary generated it accurate as there is no summary or data to compare our summary with the actual.
The summary is generated based on the above method.
