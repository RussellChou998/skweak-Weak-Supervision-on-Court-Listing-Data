# skweak: Weak Supervision on Court Listing Data
Due to the development of deep learning models, NLP has dramatically enhanced in recent years. Mishcon de Reya in the legal industry is benefiting from the use of NLP in practical applications, such as automated data extraction from unstructured court listing texts. To tailor these models to the individual legal business use cases, they still need hand-labelled training data. Therefore, it might take many months to collect the data and even longer to label it.

The aim is to extract court listing entities and automatically label the data, such as the Court Date, Court Name, Judge Name, and other court listing data by using the application of weak supervision from NLP. 

The retrieved entities were then further improved by being combined into a single CSV file using legal label functions. 

In this exploration, 200 court listing text files were used to create a dataset, and NER models were trained to convert unstructured text into structured text using an automatic labelling procedure. Form this research, Skweak is used as a Python-based software tool for weak supervision tasks to extract entities and labelled data and deploy it into a single CSV file.

To evaluate the performance of using skweak as the weak labelling toolkit, we use SpaCy to train the NER models, including Majority Voting and Generative Model (HMM) approach. In the end, we evaluate the weak labelling performance by using the best model to test the court listing data.

The exploration of this research is followed by this published paper: 
### Full Paper:
Pierre Lison, Jeremy Barnes and Aliaksandr Hubin (2021), "skweak: Weak Supervision Made Easy for NLP", ACL 2021 (System demonstrations).

## Overall Project Approach 

![image](https://user-images.githubusercontent.com/100432868/188026522-5d341dbb-f860-49c4-a57d-e64929f9264b.png)

#### Pre-processing:

1. Extract and load all the court listing text files from the provided cloud service from Mishcon de Reya LLP.

2. Use the skweak to detect the keywords in all the text file without any heuristic custom-made labelling functions and display the output with a UI interface.

#### Labelling functions process:

3. Import all the provided court listing functions into the Jupyter notebook environment to create custom-made heuristic label functions after this stage.

4. Apply the court listing functions into the skweak to create a custom-made labelling function.

5. Use the custom-made labelling functions to print out relevant keywords in the display function. So that we can see whether the keywords have been detected by the right label.

#### Data frame creation:

6. Extract all the labelled data from the text file and transform them into a data frame format.

7. Merge each court attribute into a one single data frame format.

8. Conduct manual data cleaning to remove all the inaccurate labelled data from the data frame.

#### Development of Aggregation:

9. Create a MajorityVoter object to aggregate the annotations of all the text files to get the aggregated results as a labelled corpus.

10. Create a generative model from HMM model, which is a similar step in the creation of MajorityVoter.

#### Train NER model:

11. Use MajorityVoter as a baseline model to proceed into the SpaCy training pipeline to make the prediction of the performance and accuracy level of the labelled corpus.

12. Use the generative model as another model to train on the SpaCy training pipeline based on those automated annotations.

13. Compare the predicted results from both trained models.

#### Test the trained model:

14. Load the best model on SpaCy by taking the model with best performance and run it on the text file to see the display with all the labelled text.

15. Evaluate the best model performance on each entity.
