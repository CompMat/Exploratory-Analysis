# Exploratory-Analysis
Exploratory Analysis
from mpl_toolkits.mplot3d import Axes3D
from sklearn.preprocessing import StandardScaler
import matplotlib.pyplot as plt # plotting
import numpy as np # linear algebra
import os # accessing directory structure
import pandas as pd # data processing, CSV file I/O (e.g. pd.read_csv)

print(os.listdir('../input'))

nRowsRead = 1000 # specify 'None' if want to read whole file
df1 = pd.read_csv('../input/Automobile_data.csv', delimiter=',', nrows = nRowsRead)
df1.dataframeName = 'Automobile_data.csv'
nRow, nCol = df1.shape
print(f'There are {nRow} rows and {nCol} columns')

df1.head(5)
###Distribution graphs (histogram/bar graph) of sampled columns:
plotPerColumnDistribution(df1, 10, 5)
##Correlation matrix:

plotCorrelationMatrix(df1, 8)


#Scatter and density plots:
plotScatterMatrix(df1, 20, 10)
