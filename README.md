# old_fashion_nlp

[Lisez-moi en français](LISEZMOI.md) • [Read me in English](README.md)

This depository contains various tools I use in order to pre-process texts for statistical analysis. Most of them are designed to work with French texts. In spite of the massive changes introduced in NLP by machine learning algorithms, I still think a good (manual) pre-processing of texts is key to successful text mining.

For stopwords removal, refer to the following repository : [`french_stopwords`](https://github.com/gillesbastin/french_stopwords/)

## Content

- [`numbers_in_letters`](numbers_in_letters.csv) is a csv file containing all numbers from 0 to 100, spelled as numeral (column 1) and in word form in English (column 2) and in French (column 3). It can be used to detect, count, or extract numbers from a text, regardless of the way they are spelled.
- [`cues`](cues.csv) is a CSV file containing a list of 192 verbs ("cues") used in French to introduce quotes in the press. These verbs were identified using an algorithm trained to recognize quotes, their cues, and authors within a large corpus of articles from Le Monde, encompassing all articles published between 1945 and 2021. The algorithm was developed by [Ange Richard](https://www.pacte-grenoble.fr/fr/ange-richard), and the corpus provided by [Benoît de Courson](https://regicid.github.io/). The first colum (*lemmatized_cue*) contains the infinitive of the verbs ; the second column (*cue*) contains the various conjugated forms of the verbs ; the third columns (*n*) contains the number of times each form appears in the corpus, helping to measure their frequency. Only cues with more than 200 occurrences in the entire corpus were included. The conjugated forms encompass : 1st and 3rd person singular of the present tense ; 1st and 3rd person singular of the imperfect tense ; 3rd person singular of the preterite tense ; Past participle (masculine and in some cases feminine) ; Present participle ; Infinitive. For some verbs, the list also includes common other forms or misspellings found in the corpus. This list is useful for lemmatizing media content in research focused on quotation practices. However, it is important to note that it cannot be used without precautions before part-of-speech (POS) tagging due to possible ambiguities if applied to tokens that are not verbs. The R code to manipulate verbs is provided in [`cues_code`](cues_code.txt).
- [`cues_all`](cues_all.csv) provides the same data as [`lemmatized_cues`](cues.csv), but it includes all forms of the verbs. For forms not found in the corpus, the *n* column will contain NA.
- [`gendered_occupations`](gendered_occupations.csv) contains a list of 434 occupations in French with distinct male and female versions. The occupations were identified based on the guide provided by INSEE, which illustrates the 2020 version of its nomenclature of occupations and socio-professional categories (PCS). The guidebook can be accessed [here](https://www.insee.fr/fr/statistiques/fichier/6051913/Guide_PCS_2020_version_2024.pdf). The list excludes: a) occupation names that are too ambiguous or not specific to a particular PCS (e.g., "directeur", "assistant", "chef") ; b) occupations with identical names for both men and women (e.g., "buraliste," "architecte") ; c) occupation names that could be used metaphorically rather than literally (e.g., "artisan", "acteur").

## Updates

- 2024-11-28 : Corrected spelling error ("souligner") and added missing entries ("falloir", "attendre", "refuser") in [`cues`](cues.csv) and [`cues_all`](cues_all.csv).
