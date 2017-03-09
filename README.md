# foxtrot-sentiment-analysis
Team foxtrot

https://github.com/facebookresearch/fastText
https://github.com/facebookresearch/fastText/blob/master/pretrained-vectors.md

| approach | train accuracy | test accuracy | stop words                               | stemmer/lemmatizer                   | hyperparameters | lr    | lrUpdateRate | dim | epoch | minCount | wordNgrams |  pretrainedVectors |
|----------|----------------|---------------|------------------------------------------|--------------------------------------|-----------------|-------|--------------|-----|-------|----------|------------|--------------------|
| fastText | 0.868716       | 0.817044      | nltk.corpus.stopwords                    | N                                    | default         | 0.1   | 100          | 100 | 5     | 1        | 1          | N                  |
| fastText | 0.847342       | 0.814095      | nltk.corpus.stopwords                    | nltk.stem.porter.PorterStemmer       | default         | 0.1   | 100          | 100 | 5     | 1        | 1          | N                  |
| fastText | 0.836514       | 0.808539      | nltk.corpus.stopwords                    | nltk.stem.lancaster.LancasterStemmer | default         | 0.1   | 100          | 100 | 5     | 1        | 1          | N                  |
| fastText | 0.846991       | 0.814918      | nltk.corpus.stopwords                    | nltk.stem.snowball.SnowballStemmer   | default         | 0.1   | 100          | 100 | 5     | 1        | 1          | N                  |
| fastText | 0.862346       | 0.816324      | nltk.corpus.stopwords                    | nltk.stem.wordnet.WordNetLemmatizer  | default         | 0.1   | 100          | 100 | 5     | 1        | 1          | N                  |
| fastText | 0.840463       | 0.814655      | nltk.corpus.stopwords                    | nltk.stem.wordnet.WordNetLemmatizer  | custom          | 0.01  | 50           | 100 | 13    | 10       | 1          | N                  |
| fastText | 0.836235       | 0.814174      | nltk.corpus.stopwords                    | nltk.stem.wordnet.WordNetLemmatizer  | custom          | 0.01  | 50           | 100 | 11    | 10       | 1          | N                  |
| fastText | 0.850909       | 0.815123      | nltk.corpus.stopwords                    | nltk.stem.wordnet.WordNetLemmatizer  | custom          | 0.01  | 100          | 100 | 8     | 10       | 2          | N                  |
| fastText | 0.853952       | 0.816358      | nltk.corpus.stopwords                    | nltk.stem.wordnet.WordNetLemmatizer  | custom          | 0.01  | 100          | 100 | 8     | 20       | 2          | N                  |
| fastText | 0.856199       | 0.815604      | nltk.corpus.stopwords                    | nltk.stem.wordnet.WordNetLemmatizer  | custom          | 0.01  | 100          | 100 | 8     | 50       | 2          | N                  |
| fastText | 0.854124       | 0.816667      | nltk.corpus.stopwords                    | nltk.stem.wordnet.WordNetLemmatizer  | custom          | 0.01  | 1            | 50  | 8     | 20       | 2          | N                  |
| fastText | 0.850815       | 0.817879      | N                                        | spacy.en.English                     | default         | 0.1   | 100          | 100 | 5     | 1        | 1          | N                  |
| fastText | 0.854228       | 0.815843      | nltk.corpus.stopwords                    | spacy.en.English                     | default         | 0.1   | 100          | 100 | 5     | 1        | 1          | N                  |
| fastText | 0.853178       | 0.819979      | N                                        | spacy.en.English                     | custom          | 0.1   | 100          | 300 | 5     | 1        | 1          | wiki.en            |
| fastText | 0.824509       | 0.812091      | N                                        | spacy.en.English                     | custom          | 0.01  | 100          | 300 | 5     | 1        | 1          | wiki.en            |
| fastText | 0.833534       | 0.81588       | N                                        | spacy.en.English                     | custom          | 0.01  | 100          | 300 | 8     | 1        | 1          | wiki.en            |
| fastText | 0.834378       | 0.816569      | N                                        | spacy.en.English                     | custom          | 0.01  | 100          | 300 | 8     | 20       | 1          | wiki.en            |
| fastText | 0.834447       | 0.81619       | N                                        | spacy.en.English                     | custom          | 0.01  | 100          | 300 | 8     | 30       | 1          | wiki.en            |
| fastText | 0.834464       | 0.817465      | N                                        | spacy.en.English                     | custom          | 0.01  | 100          | 300 | 8     | 100      | 1          | wiki.en            |
| fastText | 0.833267       | 0.816569      | N                                        | spacy.en.English                     | custom          | 0.01  | 100          | 300 | 8     | 500      | 1          | wiki.en            |
| fastText | 0.832863       | 0.816328      | N                                        | spacy.en.English                     | custom          | 0.005 | 100          | 300 | 15    | 500      | 1          | wiki.en            |
| fastText | 0.853817       | 0.82053       | movie                                    | spacy.en.English                     | custom          | 0.1   | 100          | 300 | 5     | 1        | 1          | wiki.en            |
| fastText | 0.832658       | 0.817568      | movie                                    | spacy.en.English                     | custom          | 0.005 | 100          | 300 | 15    | 500      | 1          | wiki.en            |
| fastText | 0.853757       | 0.819944      | movie, film etc.                         | spacy.en.English                     | custom          | 0.1   | 100          | 300 | 5     | 1        | 1          | wiki.en            |
| fastText | 0.833054       | 0.817189      | movie, film etc.                         | spacy.en.English                     | custom          | 0.005 | 100          | 300 | 15    | 500      | 1          | wiki.en            |
| fastText | 0.860124       | 0.811323      | movie, film etc. + nltk.corpus.stopwords | spacy.en.English                     | custom          | 0.1   | 100          | 300 | 5     | 1        | 1          | wiki.en            |
| fastText | 0.838971       | 0.81239       | movie, film etc. + nltk.corpus.stopwords | spacy.en.English                     | custom          | 0.005 | 100          | 300 | 15    | 500      | 1          | wiki.en            |
