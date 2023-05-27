<div align="center">

# GrammatikTAK Datasets

</div>

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />

## What is GrammatikTAK Datasets?
A collection of human annotated datasets for everyone to use distributed under the [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) license.

This is not a set of training data. There exist a large number of huge nordic datasets ([1](https://github.com/alexandrainst/danlp/blob/master/docs/docs/datasets.md), [2](https://universaldependencies.org/treebanks/da_ddt/index.html) & [3](https://github.com/fnielsen/awesome-danish))  with different kinds of data for training.

I felt that the danish NLP community could benefit from having a high-quality, human annotated dataset to use when testing NLP models or for other usage. 

I strive to make the datasets:
- Of extremely **high quality** (if you find a mistake, let us know).
- **Large**, so that the test size is big enough for you to get a reasonable accurate estimate of your models performance.
- **Broad** to capture different themes, sentence constructions and lengths.

## How to use?
You are free to use whatever file you want. Here is a description of how they are constructed: 
- Every file is focused on one specific error in the selected language (currently only danish - we would like to expand this to other nordics languages). 
- Every file has a wrong version of the sentence on the left and a correct version of the sentence on the right.

## Load a dataset:
```
df = pd.read_csv("present_tense.csv", sep="|")
```

## How has the datasets been gathered?
- Wikipedia
- Made up text
- Internal documents
- [Danish gigaword](https://gigaword.dk/)

## More information about each dataset:

**Nutids-r**:
- Every verb is written in present tense, but has two tense: present infinitive (navneform, infinitiv) and present tense (nutid).
- On the left the verb is written in the wrong tense and on the right in the right tense regardless of the issue being a nutids-r.

**Wikipedia_spelling_errors**
- Webscrabed and cleaned from [wikipedia](https://da.wikipedia.org/wiki/Wikipedia:Almindelige_stavefejl)
- As wikipedia descibes, please notice: Not all occurrences of these words may be spelling errors. For instance, if the word is in a song or book title or part of a proper name for a person, city, or company, it should be left as intended by the author. So, think twice before correcting these spelling errors.
