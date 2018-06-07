# RAKE
---

A Python implementation of the Rapid Automatic Keyword Extraction (RAKE) algorithm as described in: Rose, S., Engel, D., Cramer, N., & Cowley, W. (2010). Automatic Keyword Extraction from Individual Documents. In M. W. Berry & J. Kogan (Eds.), Text Mining: Theory and Applications: John Wiley & Sons.

The source code is released under the MIT License.

## Installing rake

To install rake as a package, run:

`python setup.py install`

## Example use

```python
from nlp_rake import rake
import nltk

rakeObj = rake.Rake(stop_words_list=nltk.corpus.stopwords.words('russian'), min_char_length=4, max_words_length=3, min_keyword_frequency=2)

rake_object = rake.Rake(stoppath, 5, 3, 4)

sample_file = open("source.txt", 'r', encoding="iso-8859-1")
text = sample_file.read()

keywords = rakeObj.run(text)

# 3. print results
print("Keywords:", keywords)
```
