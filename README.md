# Text-Preprocesser
A simple preprocessing tool for natural language processing projects.

## How to Use

- Download TextPreprocesser.py
- import to another file: from TextPreprocesser import TextPreprocesser
- Create instance: TP = TextPreprocesser()

## Parameters

- lang: which language will be preprocessed English or Turkish.<br/>If you say what's the difference, the stopwords and the letter i, the difference..<br/>Example: TextPreprocesser(lang="turkish") default is english 
- lower: Will all characters be converted to lowercase? True or False <br/>Example: TextPreprocesser(lower=False) default is True. 
- digits: Will Numbers be deleted? True or False. <br/>Example: TextPreprocesser(digits=False) default is True. 
- link: Will links be deleted? True or False.  <br/>Example: TextPreprocesser(link=False) default is True. 
- punc: Will punctuation be deleted? True or False.  <br/>Example: TextPreprocesser(punc=False) default is True.
- stem: Will stemming be done? True or False.  <br/>Example: TextPreprocesser(stem=False) default is True.
- stop_words: Will stop words be deleted? True or False. <br/>Example: TextPreprocesser(stop_words=False) default is True.
- min_length_count: Deletes shorter than word length. int. <br/>Example: TextPreprocesser(min_length_count=1) default is 2.

## Examples

```python
from TextPreprocesser import TextPreprocesser

TP = TextPreprocesser(lang="english", lower=True, digits=True, link=True, punc=True,
                 stem=True, stop_words=True, min_length_count=2)

test = "I am not an Athenian or a Greek, but a citizen of the world. -Diogenes"

result = TP.string_to_preprocessed_string(test)

print(result)
# athenian greek citizen world diogen

TP2 = TextPreprocesser(lang="english", lower=True, digits=True, link=True, punc=True,
                 stem=False, stop_words=False, min_length_count=0)

test2 = "I am not an Athenian or a Greek, but a citizen of the world. -Diogenes ref:https://www.brainyquote.com/quotes/diogenes_107020"

result2 = TP2.string_to_preprocessed_string(test)

print(result2)
# i am not an athenian or a greek  but a citizen of the world   diogenes
```
