## More information about each dataset:

<details>
<summary><h3>present_tense<h3></summary>


- Every verb is written in present tense, but has two tense: present infinitive (navneform, infinitiv) and present tense (nutid).
- On the left the verb is written in the wrong tense and on the right in the right tense regardless of the issue being a nutids-r.

Load with:
```
df = pd.read_csv("present_tense.csv", encoding="UTF-8", sep="|")
```
</details>
<details>
<summary><h3>wikipedia_spelling_errors<h3></summary>


- Webscrabed and cleaned from [wikipedia](https://da.wikipedia.org/wiki/Wikipedia:Almindelige_stavefejl)
- As wikipedia descibes, please notice: Not all occurrences of these words may be spelling errors. For instance, if the word is in a song or book title or part of a proper name for a person, city, or company, it should be left as intended by the author. So, think twice before correcting these spelling errors.

Load with:
```
df = pd.read_csv("wikipedia_spelling_errors.csv", encoding="UTF-8", sep="|")
```

</details>
<details>
<summary><h3>danish_ner<h3></summary>
    

- A large danish NER train, test and validation danish can be found [here](https://huggingface.co/datasets/dane/viewer/default)
- The intention of this is to have another dataset to test NER models. The more datasets avaliable for testing, the easier it is to find tendencies in the models mistakes and get a appropriate accuracy without having to worry about being too impacted by one datasets biases.

Load with:
```
with open("danish_ner.pickle", "rb") as file:
    df = pickle.load(file)

sentences = list(df["sentence"].values)
ner = list(df["ner"].values)
```
</details>
