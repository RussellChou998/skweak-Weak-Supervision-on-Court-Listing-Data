# skweak: Weak Supervision on Court Listing Data
Due to the development of deep learning models, NLP has dramatically enhanced in recent years. Mishcon de Reya in the legal industry is benefiting from the use of NLP in practical applications, such as automated data extraction from unstructured court listing texts. To tailor these models to the individual legal business use cases, they still need hand-labelled training data. Therefore, it might take many months to collect the data and even longer to label it.

The aim is to extract court listing entities and automatically label the data, such as the Court Date, Court Name, Judge Name, and other court listing data by using the application of weak supervision from NLP. 

The retrieved entities were then further improved by being combined into a single CSV file using legal label functions. 

In this exploration, 200 court listing text files were used to create a dataset, and NER models were trained to convert unstructured text into structured text using an automatic labelling procedure. Form this research, Skweak is used as a Python-based software tool for weak supervision tasks to extract entities and labelled data and deploy it into a single CSV file.

To evaluate the performance of using skweak as the weak labelling toolkit, we use SpaCy to train the NER models, including Majority Voting and Generative Model (HMM) approach. In the end, we evaluate the weak labelling performance by using the best model to test the court listing data.

The exploration of this research is followed by this published paper: 
### Full Paper:
Pierre Lison, Jeremy Barnes and Aliaksandr Hubin (2021), "skweak: Weak Supervision Made Easy for NLP", ACL 2021 (System demonstrations).
