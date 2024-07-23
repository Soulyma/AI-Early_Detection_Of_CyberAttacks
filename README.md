# AI-Early_Detection_Of_CyberAttacks
AI-Early_Detection_Of_CyberAttacks_Using_MachineLearning

Our findings provide critical insights into future trends in threat mitigation and incident response strategies.

Within this repository, you'll find three Jupyter Notebook files (.ipynb). The first focuses on training a
model to predict the presence of a cyberattack. The second one deals with predicting the specific type of cyberattack.

During the training process for the cyberattack type prediction model, the initial attempt yielded unsatisfactory results.
To address this, we employed the 'SMOTE' library for data augmentation. This involved applying oversampling followed by undersampling to reduce noise within the dataset.

```

from imblearn.under_sampling import EditedNearestNeighbours 

from imblearn.over_sampling import SMOTE

sm = SMOTE(sampling_strategy='all',n_jobs=-1,k_neighbors=3)


```
