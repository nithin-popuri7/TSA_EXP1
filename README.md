# Ex.No: 01 PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
### POPULATION
```
Developed By:P.Siva Naga Nithin
Reg.No:212221240037
```
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df["2015"].mean()
df.resample('Y').mean()
mean=df.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population(in Thousands)")
plt.show()
```
### MARKET PRICE
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("trainset.csv",parse_dates=["Date"],index_col="Date")
df.head()
df.Close.resample('M').mean()
mean=df.Close.resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Price")
plt.show()
mean=df.Close.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Price")
plt.show()
```
### TEMPERATURE
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("DailyDelhiClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
```
## OUTPUT
### Population
![image](https://github.com/nithin-popuri7/TSA_EXP1/assets/94154780/817971d7-b5e3-4e0c-939e-e701de2efbaa)

### Stock Price
![image](https://github.com/nithin-popuri7/TSA_EXP1/assets/94154780/dbe7d218-96c1-477d-a762-218fb50522df)


![image](https://github.com/nithin-popuri7/TSA_EXP1/assets/94154780/7713ca78-448a-4dcd-9efb-294c45ec08ab)


### Temperature

![image](https://github.com/nithin-popuri7/TSA_EXP1/assets/94154780/61ca2d92-ddbd-48da-83fe-2b792c157ffd)

# RESULT:
Thus we have created the python code for plotting the time series of given data.
