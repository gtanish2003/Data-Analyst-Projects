import numpy as np
import pandas as pd
import seaborn as sns
from matplotlib import pyplot as plt
data=pd.read_csv('Diwali Sales Data.csv',encoding='unicode_escape')
data.head()
data.info()
data.drop(['Status','unnamed1'],axis=1,inplace=True)
pd.isnull(data).sum()
data.dropna(inplace=True)
pd.isnull(data).sum()
data['Amount']=data['Amount'].astype('int')
