<div align="center">

# GrammatikTAK Datasets

</div>

## What is GrammatikTAK Datasets?
A collection of human annotated datasets for everyone to use. 

This is not a set of training data. There exist a large number of huge nordic datasets ([1](https://github.com/alexandrainst/danlp/blob/master/docs/docs/datasets.md), [2](https://universaldependencies.org/treebanks/da_ddt/index.html) & [3](https://github.com/fnielsen/awesome-danish))  with different kinds of data for training.

We felt that the danish NLP community could benefit from having a high-quality, human annotated dataset to use when testing NLP models or for other usage. 

We strive to make the datasets:
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

## More information about each dataset:

**Nutids-r**:
- Every verb is written in present tense, but has two tense: present infinitive (navneform, infinitiv) and present tense (nutid).
- On the left the verb is written in the wrong tense and on the right in the right tense regardless of the issue being a nutids-r.
