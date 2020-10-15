# model-releases
Released pre-trained models for use with RPA Tomorrow

## Installing with pip
Install the models with pip, with the correct tag/release name
```
pip install https://github.com/rpa-tomorrow/model-releases/releases/download/<TAG>.tar.gz
```

## Loading models
Once installed, you can load the models in python

```python
import spacy

nlp = spacy.load(<TAG>)
doc = nlp("send an email to Robert")
```

## Manual install
Clone the repo or download the release. Then you can manually load the model
by referring to the directory
```python
import spacy

nlp = spacy.load("/path/to/model")
```
