# old_fashion_nlp

This depository contains various tools I use in order to pre-process texts for statistical analysis. Most of them are designed to work with French texts. In spite of the massive changes introduced in NLP by machine learning algorithms, I still think a good (manual) pre-processing of texts is key to successful text mining.

For stopwords removal, refer to the following repository : [`french_stopwords`](https://github.com/gillesbastin/french_stopwords/)

- [`NUMBERS_IN_LETTERS`](numbers_in_letters.csv) is a csv file containing all numbers from 0 to 100, spelled as numeral (column 1) and in word form in English (column 2) and in French (column 3). It can be used to detect, count, or extract numbers from a text, regardless of the way they are spelled.
