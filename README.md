# Text-Preprocesser
A simple preprocessing tool for natural language processing projects.

## How to Use

- Download TextPreprocesser.py
- import to another file: from TextPreprocesser import TextPreprocesser
- Create instance: TP = TextPreprocesser()

## Parameters

- lang: which language will be preprocessed English or Turkish. If you say what's the difference, the stopwords and the letter i, the difference. Example: TextPreprocesser(lang="turkish") default english 
- lower=True
- digits=True
- link=True
- punc=True
- stem=True
- stop_words=True
- min_length_count=2
