# weka-dataset-accident
import pandas as pd
#load the dataset
data=pd.read_csv('Accidents.csv)
#Handle missing values
data.fillna(method='ffill',inplace=True)
#Convert categorical variables to numerical
data=pd.get_dummies(data, drop_first=True)
#save the prepocessed data
data.to_csv('Accidents_prepocessed.csv', index=False)

