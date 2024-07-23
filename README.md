# AI-Early_Detection_Of_CyberAttacks
AI-Early_Detection_Of_CyberAttacks_Using_MachineLearning

Our findings provide critical insights into future trends in threat mitigation and incident response
You will find three .ipynb files one for training a model for predecting if there is a cyber attack or not
and the other one to predict the kind of the cyber attack.
While training the model to predict the kind of the cyber attack, the first attempt did not give good results
for that I used the 'SMOTE' library in order to augment the data 

```

from imblearn.under_sampling import EditedNearestNeighbours 

from imblearn.over_sampling import SMOTE

sm = SMOTE(sampling_strategy='all',n_jobs=-1,k_neighbors=3)

X_res, y_res = sm.fit_resample(X, y)

freq =Counter(y_res)

print(freq)

print(Counter(y))

### Assuming X and y are your feature matrix and target vector

enn = EditedNearestNeighbours(n_jobs=-1)

X_resampled, y_resampled = enn.fit_resample(X_res, y_res)

freq =Counter(y_resampled)

print(freq)

print(Counter(y_res))

```
