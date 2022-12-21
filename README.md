# PMH-LDCT-NER-Model

This is our best-performing NER model trained for radiology NER, which was trained by 400 labeled radiology reports. 
All trained models described in our manuscript can be made available upon request.


Demo code:

import stanza
nlp = stanza.Pipeline(lang='en', processors={'ner': 'tokenize'}, ner_model_path='saved_models/Bi-LSTM_LDCT_NER.pt')
text = xxx.lower("The body of the report")
text = text.replace(", and", "and")
------other preprocessing depends on the task----------
doc = nlp(text)



and you could follow the stanza NER usage page:
https://stanfordnlp.github.io/stanza/biomed_model_usage.html
