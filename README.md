## DNS Alert Model
This repo contains the the code for the training and evaluation of a binary classifier for alerting whether 
a person is querying a malicious domain.

The `notebooks` directory contains the Jupyter Notebook where the model was trained. The `saved_models` 
directory contains the model that has achieved the maximum validation accuracy while training.

#### Training
The model was trained on the top 500 malicious domains as found in this 
[link](https://blacklist.cyberthreatcoalition.org/vetted/domain.txt) and the top 500 non-malicious (normal) domains as 
found in this [link](https://www.domcop.com/top-10-million-domains). 

The dataset was created by combining the malicious domains as well as the non-malicious. The dataset was split as
follows: 
- Train Set: 80% of the dataset.
- Validation Set: 10 % of the dataset
- Test Set: 10% of the dataset

#### Accuracy 

The accuracy for the Train Set, Validation Set and Test Set is as follows:

| Metric   | Train Set   | Validation Set | Test Set |  
|----------|-------------|----------------|----------|
| Accuracy | 99.25 %     | 98.00 %        | 98.00 %  |

The training graphs, confusion matrices and other metrics can be found in the `training_dns_alert_model.ipunb` notebook 
in the `notebooks` directory.
