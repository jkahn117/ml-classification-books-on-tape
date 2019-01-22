# Books on Tape

Classify audio books written by classic authors, Jane Austen and Charles Dickens.

## Datasets

Data will be derived by using [Amazon Transcribe](https://aws.amazon.com/transcribe/) to transcribe audio books downloaded from http://www.openculture.com/freeaudiobooks. Transcribed files will be stored in Amazon S3 and labelled with author name.

## Modeling Strategy

Transcribed data will be stored as a labelled book. Modeling will be performed at different granularities to determine the optimal tokenization strategy: sentence, paragraph, or chapter.

Will begin by leveraging BlazingText to examine the following differentiate between authors:

* Richness of vocabulary
* Word length
* Sentence length
* Use of function words

## End Goal

Intention of this project is to identify the author of Austen and Dickens books when presented with a new audio book.