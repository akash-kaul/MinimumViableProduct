# MinimumViableProduct
MVP for Core Safinia Functionality

# Resources

- https://github.com/wolfgarbe/SymSpell/blob/master/README.md
- https://www.mayoclinic.org/diseases-conditions
- https://spacy.io/universe/project/spacy_hunspell
- https://cs.pomona.edu/~dkauchak/simplification/
- https://github.com/miso-belica/sumy
- https://github.com/XingxingZhang/pysari
- https://github.com/deepmipt/DeepPavlov

# Pipeline

Twilio SMS --> MVP Script --> split by sentences --> correct minor spelling

--> figure out subject of question using SpaCy parts of speech ("What are symptoms of HIV" --> ["HIV", "Symptoms"])

--> find appropriate heading in Mayo Clinic website --> return query

# Safinia.py

Takes in text message. Splits message into sentences using SpaCy. Corrects sentence grammer/spelling with SymSpell. Determine if sentence is question or not.

# Database Intents

- Description
- Symptoms
- Testing Methodology
- Treatment Options, Average Cost of Treatment
- Cause
- Infectiousness (how it's spread)
- Risk Factors
- Prevention Measures

# Requirements

    pip install -U spacy
    python -m spacy download en_core_web_sm
    python -m spacy download en_core_web_lg # read timeout
    pip install beautifulsoup4
    python -m pip install -U symspellpy
