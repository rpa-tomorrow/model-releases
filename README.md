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
# (Maintainers) Creating a release
This is a guide for those who want to push new model releases to this repository.
1. After training and saving the model, check that the `meta.json` is correct otherwise update it with the correct information.
2. Make a PR with the model's metadata `meta.json` and place it in this repository inside `meta/`
3. To create a release package run 
```
python -m spacy package /path/to/your/trained/model /path/to/store/release
```
4. Build the model package by running the following inside `/path/to/store/release`
```
python setup.py sdist
```
5. The created tarball can be used to create a release here on Github
