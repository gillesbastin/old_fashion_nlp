# old_fashion_nlp

This depository contains various tools I use in order to pre-process texts for statistical analysis. Most of them are built to work on French texts. In spite of the lassive changes introduced in NLP by machine learning algorithms, I still think a good (manual) pre-processing of texts is key to successful text mining.

For stopwords removal, refer to the following repository : [`french_stopwords`](https://github.com/gillesbastin/french_stopwords/)

- [`NOMBRES_EN_LETTRES`](nombres_en_lettres.csv) is a csv file containing all numbers from 0 to 100, spelled as numeral (column 1) and in word form in French (column 2). It can be used to detect, count, or extract numbers from a text, regardless of the way they are spelled.
