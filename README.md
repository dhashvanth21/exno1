# Exno:1 Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
```
import pandas as pd
df = pd.read_csv('Data_set.csv')
df
```
<img width="1253" height="436" alt="{911FB474-B634-4687-B2CC-86A91D918EE2}" src="https://github.com/user-attachments/assets/2101ae21-fbdd-42fa-a89f-641a2e7b68c1" />

```
df.info()
```
<img width="565" height="357" alt="{C38801A3-F6D3-4AA4-8448-C3889DE78455}" src="https://github.com/user-attachments/assets/f9c12349-35c3-4a47-afdd-cb3ac824ee0f" />

```
df.describe()
```
<img width="800" height="309" alt="{663C8F6B-3A2E-4FA4-AA7A-79A89B21DF62}" src="https://github.com/user-attachments/assets/a7f91c0b-e53c-4989-93a5-978dde9b1fe6" />


```
df.head(3)
```
<img width="1236" height="155" alt="{73218BCC-A517-4E8A-BF6F-5BF8C28DE631}" src="https://github.com/user-attachments/assets/299e7d92-9cdb-4cc5-9e08-46fc1569a93c" />


```
df.tail(4)
```
<img width="1261" height="186" alt="{1916E794-39B1-4FCA-A3F9-D18F92003D8D}" src="https://github.com/user-attachments/assets/bf45fd60-b1a3-42c3-b41b-5f866b6c0247" />

```
df.shape
```
<img width="248" height="103" alt="{79C13C1E-45B1-4C14-9B70-6386C3F33512}" src="https://github.com/user-attachments/assets/17946ecb-8def-4710-97a6-e62675b810a8" />


```
df.isnull()
```
<img width="1096" height="448" alt="{DD3EE934-FC90-4434-93D1-62A2701797B4}" src="https://github.com/user-attachments/assets/108d7157-ce63-4088-851a-67648db088ac" />

```
df.notnull()
```
<img width="1121" height="448" alt="{C3BAFFFC-BCEC-451D-B47E-B4F456A2097A}" src="https://github.com/user-attachments/assets/bf9427cd-6ae7-44d0-8585-e7e59a8d28f5" />


```
df.isnull().sum()
```
<img width="493" height="235" alt="{BF3913DD-142C-4F59-8318-D8758B140204}" src="https://github.com/user-attachments/assets/62601c57-7591-4cd6-8936-a1a019d9bcff" />


```
df.dropna(axis=0)
```
<img width="1267" height="621" alt="{1D7F9852-8C06-48F7-9988-CCCC6DF4A0A1}" src="https://github.com/user-attachments/assets/71ed30ca-6122-4059-87b0-a4763d39ae47" />


```
df.dropna(axis=1)
```
<img width="591" height="443" alt="{BD84997F-E4A5-41FB-928D-3D67947C2C28}" src="https://github.com/user-attachments/assets/a1ddb893-842e-4a11-995a-e4d430bb48cd" />


```
dfs = df[df['lifetime_popularity_rank']>20]
dfs
```
<img width="1272" height="492" alt="{B843204E-FDE8-4720-880A-B172081975C7}" src="https://github.com/user-attachments/assets/d6e3b48e-8df5-4d64-8c5c-ecd506f9e364" />


```
df.fillna(0)
```
<img width="1260" height="449" alt="{1DEBA199-A063-4DE2-AFA9-128E69F7BBF8}" src="https://github.com/user-attachments/assets/0c133bab-6391-44cb-94a1-92700bc13a1b" />


```
df[(df['num_episodes']>20)&df['show_name'].str.startswith('A','F')]
df
```
<img width="1262" height="120" alt="{646115B3-809D-445E-A91E-CED922ECF490}" src="https://github.com/user-attachments/assets/e0797b9c-d7f6-4b8a-a925-7d2af4a40ef5" />

```
df.iloc[1:3,:3]
```
<img width="479" height="100" alt="Screenshot 2025-08-19 103209" src="https://github.com/user-attachments/assets/688795e4-b1bf-4c4d-91f3-5726ea432932" />


```
df.iloc[:4]
```
<img width="1853" height="284" alt="image" src="https://github.com/user-attachments/assets/60c9756c-d56a-4c8e-8022-27f8d3cd0724" />

```
df.iloc[[6,8,10],[1,2,3]]
```
<img width="495" height="144" alt="{2C4CB3B3-F6EE-4FB3-88EB-1AF91C366357}" src="https://github.com/user-attachments/assets/b96fe703-418b-4ae5-9c2e-22455821c42d" />


```
df = pd.read_csv('SAMPLEIDS.csv')
df
```
<img width="1396" height="1211" alt="image" src="https://github.com/user-attachments/assets/3d42eb40-aff0-46ee-b830-3318c433c913" />

```
df.shape
```
<img width="218" height="110" alt="image" src="https://github.com/user-attachments/assets/37e225db-1bce-4dff-84a9-0e1a47fe3444" />

```
df.describe()
```
<img width="1248" height="503" alt="image" src="https://github.com/user-attachments/assets/7c83d90f-d278-4a54-a0a3-ba95af91b315" />

```
df['GENDER'].value_counts()
```
<img width="373" height="136" alt="image" src="https://github.com/user-attachments/assets/9991c8ff-be45-4bbc-a596-4eade9d3686d" />

```
x1 = df.dropna(how='any')
x1
```
<img width="1371" height="763" alt="image" src="https://github.com/user-attachments/assets/e8233e41-c849-4231-b4d9-9715e7645391" />

```
res = df.dropna(subset=['M1','M2','M3','M4'],how='any')
res
```
<img width="1363" height="769" alt="image" src="https://github.com/user-attachments/assets/ea27b9c2-81d2-47c5-b093-c05a8067e620" />

## Outlier Detection & Removal

```
import pandas as pd
df = pd.read_csv("heights.csv")
df
```

<img width="213" height="683" alt="image" src="https://github.com/user-attachments/assets/6268ba37-fd7d-471d-a024-c34863dd905f" />

```
import seaborn as sns
sns.boxplot(data=df)
```

<img width="824" height="620" alt="image" src="https://github.com/user-attachments/assets/2090aeb3-a088-4da1-b653-4d9ec0d30e4b" />

```
sns.scatterplot(data=df)
```

<img width="826" height="649" alt="image" src="https://github.com/user-attachments/assets/94f059ac-c116-431c-9f2f-a6754ffb669b" />

```
max = df['height'].quantile(0.75)
min = df['height'].quantile(0.25)
iqr = max - min
print(iqr)
```

<img width="458" height="172" alt="image" src="https://github.com/user-attachments/assets/6706172f-f889-4bba-a0ee-366e2bb8b645" />

```
lb = min - 1.5 * iqr
ub = max + 1.5 * iqr
outliers = df[(df['height']<lb)|(df['height']>ub)]
print("Lower bound = ",lb)
print("Upper bound = ",ub)
print("Outliers: ",outliers)
```

<img width="595" height="340" alt="image" src="https://github.com/user-attachments/assets/0e6443a5-b813-41df-aeb4-a5d8cbf8b7b6" />

```
no_outliers = df[~((df['height']<lb)|(df['height']>ub))]
no_outliers
```

<img width="673" height="713" alt="image" src="https://github.com/user-attachments/assets/0ab8af17-7e8d-40d6-8681-4fd068e62cdb" />

```
sns.boxplot(data=no_outliers)
```

<img width="822" height="670" alt="image" src="https://github.com/user-attachments/assets/8636f7c2-e730-45d8-91a4-a293186ed9ef" />

```
sns.scatterplot(data=no_outliers)
```

<img width="787" height="692" alt="image" src="https://github.com/user-attachments/assets/faeca148-8c75-42f9-bb19-407f3e2f0062" />

```
import matplotlib.pyplot as plt
df
```

<img width="490" height="740" alt="image" src="https://github.com/user-attachments/assets/15cec454-28b7-4213-ac64-f3d87b68b7de" />

```
max = df['height'].quantile(0.75)
q2 = df['height'].quantile(0.5)
min = df['height'].quantile(0.25)
iqr = max - min
lb = min - 1.5 * iqr
ub = max + 1.5 * iqr
dfs = df[(df['height']>=lb)&(df['height']<=ub)]
dfs
```

<img width="524" height="792" alt="image" src="https://github.com/user-attachments/assets/42456aa6-1317-4b2e-973f-74edd6a8c0f9" />

```
import numpy as np
from scipy import stats
z = np.abs(stats.zscore(df['height']))
print(z)
```

<img width="755" height="187" alt="image" src="https://github.com/user-attachments/assets/2a109653-80ae-441a-81b2-9c06a7b4d768" />

```
df1 = df[z<3]
df1
```

<img width="296" height="683" alt="image" src="https://github.com/user-attachments/assets/c3349cba-8329-412a-afbf-f6ff1c2a1726" />

```
val = df['height']
val
```

<img width="393" height="467" alt="image" src="https://github.com/user-attachments/assets/58ea6e9c-194a-4a57-9855-e7d13707dae5" />

```
out=[]
def d_o(val):
    ts = 3
    m = np.mean(val)
    sd = np.std(val)
    for i in val:
        z = (i-m)/sd
        if np.abs(z)>ts:
            out.append(i)
    return out
op = d_o(val)
op
```

<img width="385" height="397" alt="image" src="https://github.com/user-attachments/assets/e29b9912-70ae-4e26-b3c7-54dcc640e9ce" />






# Result
          
The given data has been read and data has been cleaned and the data has been saved to a file.

