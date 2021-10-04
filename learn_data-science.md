```python
import pandas as pd
import matplotlib.pyplot as mpl
```

## **Creating charter/plot**

# **Series VS. DataFrame**

## **Data Series**
### ***Series is one dimensional (One Coulmn)***
#### **Can be created ONLY from Lists** 


```python
car_Brand = pd.Series(["BMW", "Nissan", "Toyota", "Honda"])
car_Brand
```




    0       BMW
    1    Nissan
    2    Toyota
    3     Honda
    dtype: object




```python
colors = pd.Series(["Blue", "Red", "Green", "Yellow"])
colors
```




    0      Blue
    1       Red
    2     Green
    3    Yellow
    dtype: object



## **Creating DataFrame from Importing Data** 


```python
df = pd.read_csv("042 heart-disease.csv")
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>age</th>
      <th>sex</th>
      <th>cp</th>
      <th>trestbps</th>
      <th>chol</th>
      <th>fbs</th>
      <th>restecg</th>
      <th>thalach</th>
      <th>exang</th>
      <th>oldpeak</th>
      <th>slope</th>
      <th>ca</th>
      <th>thal</th>
      <th>target</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>63</td>
      <td>1</td>
      <td>3</td>
      <td>145</td>
      <td>233</td>
      <td>1</td>
      <td>0</td>
      <td>150</td>
      <td>0</td>
      <td>2.3</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>37</td>
      <td>1</td>
      <td>2</td>
      <td>130</td>
      <td>250</td>
      <td>0</td>
      <td>1</td>
      <td>187</td>
      <td>0</td>
      <td>3.5</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>41</td>
      <td>0</td>
      <td>1</td>
      <td>130</td>
      <td>204</td>
      <td>0</td>
      <td>0</td>
      <td>172</td>
      <td>0</td>
      <td>1.4</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>56</td>
      <td>1</td>
      <td>1</td>
      <td>120</td>
      <td>236</td>
      <td>0</td>
      <td>1</td>
      <td>178</td>
      <td>0</td>
      <td>0.8</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>57</td>
      <td>0</td>
      <td>0</td>
      <td>120</td>
      <td>354</td>
      <td>0</td>
      <td>1</td>
      <td>163</td>
      <td>1</td>
      <td>0.6</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>298</th>
      <td>57</td>
      <td>0</td>
      <td>0</td>
      <td>140</td>
      <td>241</td>
      <td>0</td>
      <td>1</td>
      <td>123</td>
      <td>1</td>
      <td>0.2</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>299</th>
      <td>45</td>
      <td>1</td>
      <td>3</td>
      <td>110</td>
      <td>264</td>
      <td>0</td>
      <td>1</td>
      <td>132</td>
      <td>0</td>
      <td>1.2</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>300</th>
      <td>68</td>
      <td>1</td>
      <td>0</td>
      <td>144</td>
      <td>193</td>
      <td>1</td>
      <td>1</td>
      <td>141</td>
      <td>0</td>
      <td>3.4</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>301</th>
      <td>57</td>
      <td>1</td>
      <td>0</td>
      <td>130</td>
      <td>131</td>
      <td>0</td>
      <td>1</td>
      <td>115</td>
      <td>1</td>
      <td>1.2</td>
      <td>1</td>
      <td>1</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>302</th>
      <td>57</td>
      <td>0</td>
      <td>1</td>
      <td>130</td>
      <td>236</td>
      <td>0</td>
      <td>0</td>
      <td>174</td>
      <td>0</td>
      <td>0.0</td>
      <td>1</td>
      <td>1</td>
      <td>2</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>303 rows × 14 columns</p>
</div>




```python
df.target.value_counts().plot(kind="bar")
```




    <AxesSubplot:>




    
![svg](learn_data-science_files/learn_data-science_8_1.svg)
    



```python
car_sales = pd.read_csv("051 car-sales.csv")
car_sales
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Toyota</td>
      <td>White</td>
      <td>150043</td>
      <td>4</td>
      <td>$4,000.00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Honda</td>
      <td>Red</td>
      <td>87899</td>
      <td>4</td>
      <td>$5,000.00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Toyota</td>
      <td>Blue</td>
      <td>32549</td>
      <td>3</td>
      <td>$7,000.00</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BMW</td>
      <td>Black</td>
      <td>11179</td>
      <td>5</td>
      <td>$22,000.00</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Nissan</td>
      <td>White</td>
      <td>213095</td>
      <td>4</td>
      <td>$3,500.00</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Toyota</td>
      <td>Green</td>
      <td>99213</td>
      <td>4</td>
      <td>$4,500.00</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Honda</td>
      <td>Blue</td>
      <td>45698</td>
      <td>4</td>
      <td>$7,500.00</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Honda</td>
      <td>Blue</td>
      <td>54738</td>
      <td>4</td>
      <td>$7,000.00</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Toyota</td>
      <td>White</td>
      <td>60000</td>
      <td>4</td>
      <td>$6,250.00</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Nissan</td>
      <td>White</td>
      <td>31600</td>
      <td>4</td>
      <td>$9,700.00</td>
    </tr>
  </tbody>
</table>
</div>



# **Describe Data**

## ***Data Type***
### **.dtype is an Atribute**


```python
car_sales.dtypes
```




    Make             object
    Colour           object
    Odometer (KM)     int64
    Doors             int64
    Price            object
    dtype: object




```python
car_sales.columns
```




    Index(['Make', 'Colour', 'Odometer (KM)', 'Doors', 'Price'], dtype='object')



## **.describe() is a function that give us statistical information about numeric columns**


```python
car_sales.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>10.000000</td>
      <td>10.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>78601.400000</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>std</th>
      <td>61983.471735</td>
      <td>0.471405</td>
    </tr>
    <tr>
      <th>min</th>
      <td>11179.000000</td>
      <td>3.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>35836.250000</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>57369.000000</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>96384.500000</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>213095.000000</td>
      <td>5.000000</td>
    </tr>
  </tbody>
</table>
</div>



## **.inf() is .dtype + .index**


```python
car_sales.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 10 entries, 0 to 9
    Data columns (total 5 columns):
     #   Column         Non-Null Count  Dtype 
    ---  ------         --------------  ----- 
     0   Make           10 non-null     object
     1   Colour         10 non-null     object
     2   Odometer (KM)  10 non-null     int64 
     3   Doors          10 non-null     int64 
     4   Price          10 non-null     object
    dtypes: int64(2), object(3)
    memory usage: 528.0+ bytes
    


```python
car_sales.sum()
```




    Make             ToyotaHondaToyotaBMWNissanToyotaHondaHondaToyo...
    Colour               WhiteRedBlueBlackWhiteGreenBlueBlueWhiteWhite
    Odometer (KM)                                               786014
    Doors                                                           40
    Price            $4,000.00$5,000.00$7,000.00$22,000.00$3,500.00...
    dtype: object




```python
car_sales.mean()
```

    C:\Users\ali19\AppData\Local\Temp/ipykernel_3028/4073448239.py:1: FutureWarning: Dropping of nuisance columns in DataFrame reductions (with 'numeric_only=None') is deprecated; in a future version this will raise TypeError.  Select only valid columns before calling the reduction.
      car_sales.mean()
    




    Odometer (KM)    78601.4
    Doors                4.0
    dtype: float64




```python
car_sales.Doors.mean()
```




    4.0




```python
car_sales["Odometer (KM)"].mean()
```




    78601.4



# **Viewing & Selecting Data**


```python
car_sales.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Toyota</td>
      <td>White</td>
      <td>150043</td>
      <td>4</td>
      <td>$4,000.00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Honda</td>
      <td>Red</td>
      <td>87899</td>
      <td>4</td>
      <td>$5,000.00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Toyota</td>
      <td>Blue</td>
      <td>32549</td>
      <td>3</td>
      <td>$7,000.00</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BMW</td>
      <td>Black</td>
      <td>11179</td>
      <td>5</td>
      <td>$22,000.00</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Nissan</td>
      <td>White</td>
      <td>213095</td>
      <td>4</td>
      <td>$3,500.00</td>
    </tr>
  </tbody>
</table>
</div>




```python
car_sales.tail()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>5</th>
      <td>Toyota</td>
      <td>Green</td>
      <td>99213</td>
      <td>4</td>
      <td>$4,500.00</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Honda</td>
      <td>Blue</td>
      <td>45698</td>
      <td>4</td>
      <td>$7,500.00</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Honda</td>
      <td>Blue</td>
      <td>54738</td>
      <td>4</td>
      <td>$7,000.00</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Toyota</td>
      <td>White</td>
      <td>60000</td>
      <td>4</td>
      <td>$6,250.00</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Nissan</td>
      <td>White</td>
      <td>31600</td>
      <td>4</td>
      <td>$9,700.00</td>
    </tr>
  </tbody>
</table>
</div>




```python
car_sales.head(7)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Toyota</td>
      <td>White</td>
      <td>150043</td>
      <td>4</td>
      <td>$4,000.00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Honda</td>
      <td>Red</td>
      <td>87899</td>
      <td>4</td>
      <td>$5,000.00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Toyota</td>
      <td>Blue</td>
      <td>32549</td>
      <td>3</td>
      <td>$7,000.00</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BMW</td>
      <td>Black</td>
      <td>11179</td>
      <td>5</td>
      <td>$22,000.00</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Nissan</td>
      <td>White</td>
      <td>213095</td>
      <td>4</td>
      <td>$3,500.00</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Toyota</td>
      <td>Green</td>
      <td>99213</td>
      <td>4</td>
      <td>$4,500.00</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Honda</td>
      <td>Blue</td>
      <td>45698</td>
      <td>4</td>
      <td>$7,500.00</td>
    </tr>
  </tbody>
</table>
</div>



# **Indexing**

## ***.loc vs .iloc***
### **.iloc return DATA at position number 'acording to POSITION'**
### **.loc return DATA at specific index number 'acording to INDEX number'**


```python
animals = pd.Series(["Panda", "Snake", "Turtle", "Cat", "Bird", "Rabbit"], index=[5, 6, 8, 9, 2, 5])
print(animals)
print("==============")
print(animals.iloc[5])
print("==============")
print(animals.loc[5])
```

    5     Panda
    6     Snake
    8    Turtle
    9       Cat
    2      Bird
    5    Rabbit
    dtype: object
    ==============
    Rabbit
    ==============
    5     Panda
    5    Rabbit
    dtype: object
    


```python
car_sales.loc[4]
```




    Make                Nissan
    Colour               White
    Odometer (KM)       213095
    Doors                    4
    Price            $3,500.00
    Name: 4, dtype: object



# ***Using Slicing with .loc/.iloc*** 


```python
print(animals)
print("========POS=======")
print(animals.iloc[:2])
print("=======IND========")
print(animals.loc[:2])
print("=======IND========")
print(animals.loc[2:])
print("===============")
```

    5     Panda
    6     Snake
    8    Turtle
    9       Cat
    2      Bird
    5    Rabbit
    dtype: object
    ========POS=======
    5    Panda
    6    Snake
    dtype: object
    =======IND========
    5     Panda
    6     Snake
    8    Turtle
    9       Cat
    2      Bird
    dtype: object
    =======IND========
    2      Bird
    5    Rabbit
    dtype: object
    ===============
    


```python
animals.iloc[::2]
```




    5     Panda
    8    Turtle
    2      Bird
    dtype: object



## ***Viewing Specific Row***


```python
car_sales[car_sales["Make"] == "Toyota"]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Toyota</td>
      <td>White</td>
      <td>150043</td>
      <td>4</td>
      <td>$4,000.00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Toyota</td>
      <td>Blue</td>
      <td>32549</td>
      <td>3</td>
      <td>$7,000.00</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Toyota</td>
      <td>Green</td>
      <td>99213</td>
      <td>4</td>
      <td>$4,500.00</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Toyota</td>
      <td>White</td>
      <td>60000</td>
      <td>4</td>
      <td>$6,250.00</td>
    </tr>
  </tbody>
</table>
</div>




```python
car_sales[car_sales.Make == "Toyota"]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Toyota</td>
      <td>White</td>
      <td>150043</td>
      <td>4</td>
      <td>$4,000.00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Toyota</td>
      <td>Blue</td>
      <td>32549</td>
      <td>3</td>
      <td>$7,000.00</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Toyota</td>
      <td>Green</td>
      <td>99213</td>
      <td>4</td>
      <td>$4,500.00</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Toyota</td>
      <td>White</td>
      <td>60000</td>
      <td>4</td>
      <td>$6,250.00</td>
    </tr>
  </tbody>
</table>
</div>




```python
car_sales[car_sales["Odometer (KM)"] > 100000]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Toyota</td>
      <td>White</td>
      <td>150043</td>
      <td>4</td>
      <td>$4,000.00</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Nissan</td>
      <td>White</td>
      <td>213095</td>
      <td>4</td>
      <td>$3,500.00</td>
    </tr>
  </tbody>
</table>
</div>



# ***Manipulating Data***


```python
car_sales.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Toyota</td>
      <td>White</td>
      <td>150043</td>
      <td>4</td>
      <td>$4,000.00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Honda</td>
      <td>Red</td>
      <td>87899</td>
      <td>4</td>
      <td>$5,000.00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Toyota</td>
      <td>Blue</td>
      <td>32549</td>
      <td>3</td>
      <td>$7,000.00</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BMW</td>
      <td>Black</td>
      <td>11179</td>
      <td>5</td>
      <td>$22,000.00</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Nissan</td>
      <td>White</td>
      <td>213095</td>
      <td>4</td>
      <td>$3,500.00</td>
    </tr>
  </tbody>
</table>
</div>




```python
car_sales.Make.str.lower()
```




    0    toyota
    1     honda
    2    toyota
    3       bmw
    4    nissan
    5    toyota
    6     honda
    7     honda
    8    toyota
    9    nissan
    Name: Make, dtype: object




```python
car_sales.Make = car_sales.Make.str.upper()
car_sales
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>TOYOTA</td>
      <td>White</td>
      <td>150043</td>
      <td>4</td>
      <td>$4,000.00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>HONDA</td>
      <td>Red</td>
      <td>87899</td>
      <td>4</td>
      <td>$5,000.00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>TOYOTA</td>
      <td>Blue</td>
      <td>32549</td>
      <td>3</td>
      <td>$7,000.00</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BMW</td>
      <td>Black</td>
      <td>11179</td>
      <td>5</td>
      <td>$22,000.00</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NISSAN</td>
      <td>White</td>
      <td>213095</td>
      <td>4</td>
      <td>$3,500.00</td>
    </tr>
    <tr>
      <th>5</th>
      <td>TOYOTA</td>
      <td>Green</td>
      <td>99213</td>
      <td>4</td>
      <td>$4,500.00</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HONDA</td>
      <td>Blue</td>
      <td>45698</td>
      <td>4</td>
      <td>$7,500.00</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HONDA</td>
      <td>Blue</td>
      <td>54738</td>
      <td>4</td>
      <td>$7,000.00</td>
    </tr>
    <tr>
      <th>8</th>
      <td>TOYOTA</td>
      <td>White</td>
      <td>60000</td>
      <td>4</td>
      <td>$6,250.00</td>
    </tr>
    <tr>
      <th>9</th>
      <td>NISSAN</td>
      <td>White</td>
      <td>31600</td>
      <td>4</td>
      <td>$9,700.00</td>
    </tr>
  </tbody>
</table>
</div>



# **Fill Missing Data**


```python
car_sales_missing = pd.read_csv("053 car-sales-missing-data.csv")
car_sales_missing
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer</th>
      <th>Doors</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Toyota</td>
      <td>White</td>
      <td>150043.0</td>
      <td>4.0</td>
      <td>$4,000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Honda</td>
      <td>Red</td>
      <td>87899.0</td>
      <td>4.0</td>
      <td>$5,000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Toyota</td>
      <td>Blue</td>
      <td>NaN</td>
      <td>3.0</td>
      <td>$7,000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BMW</td>
      <td>Black</td>
      <td>11179.0</td>
      <td>5.0</td>
      <td>$22,000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Nissan</td>
      <td>White</td>
      <td>213095.0</td>
      <td>4.0</td>
      <td>$3,500</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Toyota</td>
      <td>Green</td>
      <td>NaN</td>
      <td>4.0</td>
      <td>$4,500</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Honda</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4.0</td>
      <td>$7,500</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Honda</td>
      <td>Blue</td>
      <td>NaN</td>
      <td>4.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Toyota</td>
      <td>White</td>
      <td>60000.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>NaN</td>
      <td>White</td>
      <td>31600.0</td>
      <td>4.0</td>
      <td>$9,700</td>
    </tr>
  </tbody>
</table>
</div>




```python
car_sales_missing.Doors.fillna(car_sales_missing.Doors.mean(), inplace= True)
car_sales_missing
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer</th>
      <th>Doors</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Toyota</td>
      <td>White</td>
      <td>150043.0</td>
      <td>4.0</td>
      <td>$4,000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Honda</td>
      <td>Red</td>
      <td>87899.0</td>
      <td>4.0</td>
      <td>$5,000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Toyota</td>
      <td>Blue</td>
      <td>NaN</td>
      <td>3.0</td>
      <td>$7,000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BMW</td>
      <td>Black</td>
      <td>11179.0</td>
      <td>5.0</td>
      <td>$22,000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Nissan</td>
      <td>White</td>
      <td>213095.0</td>
      <td>4.0</td>
      <td>$3,500</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Toyota</td>
      <td>Green</td>
      <td>NaN</td>
      <td>4.0</td>
      <td>$4,500</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Honda</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4.0</td>
      <td>$7,500</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Honda</td>
      <td>Blue</td>
      <td>NaN</td>
      <td>4.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Toyota</td>
      <td>White</td>
      <td>60000.0</td>
      <td>4.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>NaN</td>
      <td>White</td>
      <td>31600.0</td>
      <td>4.0</td>
      <td>$9,700</td>
    </tr>
  </tbody>
</table>
</div>




```python
print(car_sales_missing.Odometer.mean())
car_sales_missing["Odometer"].fillna(car_sales_missing["Odometer"].mean(), inplace=True)
car_sales_missing
```

    92302.66666666667
    




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer</th>
      <th>Doors</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Toyota</td>
      <td>White</td>
      <td>150043.000000</td>
      <td>4.0</td>
      <td>$4,000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Honda</td>
      <td>Red</td>
      <td>87899.000000</td>
      <td>4.0</td>
      <td>$5,000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Toyota</td>
      <td>Blue</td>
      <td>92302.666667</td>
      <td>3.0</td>
      <td>$7,000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BMW</td>
      <td>Black</td>
      <td>11179.000000</td>
      <td>5.0</td>
      <td>$22,000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Nissan</td>
      <td>White</td>
      <td>213095.000000</td>
      <td>4.0</td>
      <td>$3,500</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Toyota</td>
      <td>Green</td>
      <td>92302.666667</td>
      <td>4.0</td>
      <td>$4,500</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Honda</td>
      <td>NaN</td>
      <td>92302.666667</td>
      <td>4.0</td>
      <td>$7,500</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Honda</td>
      <td>Blue</td>
      <td>92302.666667</td>
      <td>4.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Toyota</td>
      <td>White</td>
      <td>60000.000000</td>
      <td>4.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>NaN</td>
      <td>White</td>
      <td>31600.000000</td>
      <td>4.0</td>
      <td>$9,700</td>
    </tr>
  </tbody>
</table>
</div>



## **Drop missing items**


```python
car_sales_missing.dropna(inplace=True)
car_sales_missing
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer</th>
      <th>Doors</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Toyota</td>
      <td>White</td>
      <td>150043.000000</td>
      <td>4.0</td>
      <td>$4,000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Honda</td>
      <td>Red</td>
      <td>87899.000000</td>
      <td>4.0</td>
      <td>$5,000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Toyota</td>
      <td>Blue</td>
      <td>92302.666667</td>
      <td>3.0</td>
      <td>$7,000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BMW</td>
      <td>Black</td>
      <td>11179.000000</td>
      <td>5.0</td>
      <td>$22,000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Nissan</td>
      <td>White</td>
      <td>213095.000000</td>
      <td>4.0</td>
      <td>$3,500</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Toyota</td>
      <td>Green</td>
      <td>92302.666667</td>
      <td>4.0</td>
      <td>$4,500</td>
    </tr>
  </tbody>
</table>
</div>




```python
car_sales_missing.to_csv("Car_sales_Droped_missing_items.csv")
```

# **Adding Data**


```python
Seats = pd.Series([5, 5, 5, 5, 5])
car_sales["Seats"] = Seats
car_sales
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
      <th>Price</th>
      <th>Seats</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>TOYOTA</td>
      <td>White</td>
      <td>150043</td>
      <td>4</td>
      <td>$4,000.00</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>HONDA</td>
      <td>Red</td>
      <td>87899</td>
      <td>4</td>
      <td>$5,000.00</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>TOYOTA</td>
      <td>Blue</td>
      <td>32549</td>
      <td>3</td>
      <td>$7,000.00</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BMW</td>
      <td>Black</td>
      <td>11179</td>
      <td>5</td>
      <td>$22,000.00</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NISSAN</td>
      <td>White</td>
      <td>213095</td>
      <td>4</td>
      <td>$3,500.00</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>TOYOTA</td>
      <td>Green</td>
      <td>99213</td>
      <td>4</td>
      <td>$4,500.00</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HONDA</td>
      <td>Blue</td>
      <td>45698</td>
      <td>4</td>
      <td>$7,500.00</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HONDA</td>
      <td>Blue</td>
      <td>54738</td>
      <td>4</td>
      <td>$7,000.00</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>8</th>
      <td>TOYOTA</td>
      <td>White</td>
      <td>60000</td>
      <td>4</td>
      <td>$6,250.00</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>NISSAN</td>
      <td>White</td>
      <td>31600</td>
      <td>4</td>
      <td>$9,700.00</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
car_sales["Seats"].fillna(5, inplace= True)
car_sales
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
      <th>Price</th>
      <th>Seats</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>TOYOTA</td>
      <td>White</td>
      <td>150043</td>
      <td>4</td>
      <td>$4,000.00</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>HONDA</td>
      <td>Red</td>
      <td>87899</td>
      <td>4</td>
      <td>$5,000.00</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>TOYOTA</td>
      <td>Blue</td>
      <td>32549</td>
      <td>3</td>
      <td>$7,000.00</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BMW</td>
      <td>Black</td>
      <td>11179</td>
      <td>5</td>
      <td>$22,000.00</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NISSAN</td>
      <td>White</td>
      <td>213095</td>
      <td>4</td>
      <td>$3,500.00</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>TOYOTA</td>
      <td>Green</td>
      <td>99213</td>
      <td>4</td>
      <td>$4,500.00</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HONDA</td>
      <td>Blue</td>
      <td>45698</td>
      <td>4</td>
      <td>$7,500.00</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HONDA</td>
      <td>Blue</td>
      <td>54738</td>
      <td>4</td>
      <td>$7,000.00</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>TOYOTA</td>
      <td>White</td>
      <td>60000</td>
      <td>4</td>
      <td>$6,250.00</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>NISSAN</td>
      <td>White</td>
      <td>31600</td>
      <td>4</td>
      <td>$9,700.00</td>
      <td>5.0</td>
    </tr>
  </tbody>
</table>
</div>



## ***python list MUST fill ALL column's cells***


```python
car_sales["Fule_Consumbtion"] = [9.7, 5.2, 6.5, 4.45, 3.6, 7.5, 8.2, 4.9, 7.8, 3.32]
car_sales
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
      <th>Price</th>
      <th>Seats</th>
      <th>Fule_Consumbtion</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>TOYOTA</td>
      <td>White</td>
      <td>150043</td>
      <td>4</td>
      <td>$4,000.00</td>
      <td>5.0</td>
      <td>9.70</td>
    </tr>
    <tr>
      <th>1</th>
      <td>HONDA</td>
      <td>Red</td>
      <td>87899</td>
      <td>4</td>
      <td>$5,000.00</td>
      <td>5.0</td>
      <td>5.20</td>
    </tr>
    <tr>
      <th>2</th>
      <td>TOYOTA</td>
      <td>Blue</td>
      <td>32549</td>
      <td>3</td>
      <td>$7,000.00</td>
      <td>5.0</td>
      <td>6.50</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BMW</td>
      <td>Black</td>
      <td>11179</td>
      <td>5</td>
      <td>$22,000.00</td>
      <td>5.0</td>
      <td>4.45</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NISSAN</td>
      <td>White</td>
      <td>213095</td>
      <td>4</td>
      <td>$3,500.00</td>
      <td>5.0</td>
      <td>3.60</td>
    </tr>
    <tr>
      <th>5</th>
      <td>TOYOTA</td>
      <td>Green</td>
      <td>99213</td>
      <td>4</td>
      <td>$4,500.00</td>
      <td>5.0</td>
      <td>7.50</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HONDA</td>
      <td>Blue</td>
      <td>45698</td>
      <td>4</td>
      <td>$7,500.00</td>
      <td>5.0</td>
      <td>8.20</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HONDA</td>
      <td>Blue</td>
      <td>54738</td>
      <td>4</td>
      <td>$7,000.00</td>
      <td>5.0</td>
      <td>4.90</td>
    </tr>
    <tr>
      <th>8</th>
      <td>TOYOTA</td>
      <td>White</td>
      <td>60000</td>
      <td>4</td>
      <td>$6,250.00</td>
      <td>5.0</td>
      <td>7.80</td>
    </tr>
    <tr>
      <th>9</th>
      <td>NISSAN</td>
      <td>White</td>
      <td>31600</td>
      <td>4</td>
      <td>$9,700.00</td>
      <td>5.0</td>
      <td>3.32</td>
    </tr>
  </tbody>
</table>
</div>




```python
car_sales["Fule_Used"] = car_sales["Odometer (KM)"] /100 * car_sales.Fule_Consumbtion
car_sales
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
      <th>Price</th>
      <th>Seats</th>
      <th>Fule_Consumbtion</th>
      <th>Fule_Used</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>TOYOTA</td>
      <td>White</td>
      <td>150043</td>
      <td>4</td>
      <td>$4,000.00</td>
      <td>5.0</td>
      <td>9.70</td>
      <td>14554.1710</td>
    </tr>
    <tr>
      <th>1</th>
      <td>HONDA</td>
      <td>Red</td>
      <td>87899</td>
      <td>4</td>
      <td>$5,000.00</td>
      <td>5.0</td>
      <td>5.20</td>
      <td>4570.7480</td>
    </tr>
    <tr>
      <th>2</th>
      <td>TOYOTA</td>
      <td>Blue</td>
      <td>32549</td>
      <td>3</td>
      <td>$7,000.00</td>
      <td>5.0</td>
      <td>6.50</td>
      <td>2115.6850</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BMW</td>
      <td>Black</td>
      <td>11179</td>
      <td>5</td>
      <td>$22,000.00</td>
      <td>5.0</td>
      <td>4.45</td>
      <td>497.4655</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NISSAN</td>
      <td>White</td>
      <td>213095</td>
      <td>4</td>
      <td>$3,500.00</td>
      <td>5.0</td>
      <td>3.60</td>
      <td>7671.4200</td>
    </tr>
    <tr>
      <th>5</th>
      <td>TOYOTA</td>
      <td>Green</td>
      <td>99213</td>
      <td>4</td>
      <td>$4,500.00</td>
      <td>5.0</td>
      <td>7.50</td>
      <td>7440.9750</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HONDA</td>
      <td>Blue</td>
      <td>45698</td>
      <td>4</td>
      <td>$7,500.00</td>
      <td>5.0</td>
      <td>8.20</td>
      <td>3747.2360</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HONDA</td>
      <td>Blue</td>
      <td>54738</td>
      <td>4</td>
      <td>$7,000.00</td>
      <td>5.0</td>
      <td>4.90</td>
      <td>2682.1620</td>
    </tr>
    <tr>
      <th>8</th>
      <td>TOYOTA</td>
      <td>White</td>
      <td>60000</td>
      <td>4</td>
      <td>$6,250.00</td>
      <td>5.0</td>
      <td>7.80</td>
      <td>4680.0000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>NISSAN</td>
      <td>White</td>
      <td>31600</td>
      <td>4</td>
      <td>$9,700.00</td>
      <td>5.0</td>
      <td>3.32</td>
      <td>1049.1200</td>
    </tr>
  </tbody>
</table>
</div>



## ***Droping Columns***


```python
car_sales.drop("Seats", axis=1, inplace=True)
car_sales
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
      <th>Price</th>
      <th>Fule_Consumbtion</th>
      <th>Fule_Used</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>TOYOTA</td>
      <td>White</td>
      <td>150043</td>
      <td>4</td>
      <td>$4,000.00</td>
      <td>9.70</td>
      <td>14554.1710</td>
    </tr>
    <tr>
      <th>1</th>
      <td>HONDA</td>
      <td>Red</td>
      <td>87899</td>
      <td>4</td>
      <td>$5,000.00</td>
      <td>5.20</td>
      <td>4570.7480</td>
    </tr>
    <tr>
      <th>2</th>
      <td>TOYOTA</td>
      <td>Blue</td>
      <td>32549</td>
      <td>3</td>
      <td>$7,000.00</td>
      <td>6.50</td>
      <td>2115.6850</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BMW</td>
      <td>Black</td>
      <td>11179</td>
      <td>5</td>
      <td>$22,000.00</td>
      <td>4.45</td>
      <td>497.4655</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NISSAN</td>
      <td>White</td>
      <td>213095</td>
      <td>4</td>
      <td>$3,500.00</td>
      <td>3.60</td>
      <td>7671.4200</td>
    </tr>
    <tr>
      <th>5</th>
      <td>TOYOTA</td>
      <td>Green</td>
      <td>99213</td>
      <td>4</td>
      <td>$4,500.00</td>
      <td>7.50</td>
      <td>7440.9750</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HONDA</td>
      <td>Blue</td>
      <td>45698</td>
      <td>4</td>
      <td>$7,500.00</td>
      <td>8.20</td>
      <td>3747.2360</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HONDA</td>
      <td>Blue</td>
      <td>54738</td>
      <td>4</td>
      <td>$7,000.00</td>
      <td>4.90</td>
      <td>2682.1620</td>
    </tr>
    <tr>
      <th>8</th>
      <td>TOYOTA</td>
      <td>White</td>
      <td>60000</td>
      <td>4</td>
      <td>$6,250.00</td>
      <td>7.80</td>
      <td>4680.0000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>NISSAN</td>
      <td>White</td>
      <td>31600</td>
      <td>4</td>
      <td>$9,700.00</td>
      <td>3.32</td>
      <td>1049.1200</td>
    </tr>
  </tbody>
</table>
</div>




```python
car_sales["Fule Consum."] = car_sales.Fule_Consumbtion
car_sales = car_sales.drop("Fule_Consumbtion", axis=1)
car_sales
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Make</th>
      <th>Colour</th>
      <th>Odometer (KM)</th>
      <th>Doors</th>
      <th>Price</th>
      <th>Fule_Used</th>
      <th>Fule Consum.</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>TOYOTA</td>
      <td>White</td>
      <td>150043</td>
      <td>4</td>
      <td>$4,000.00</td>
      <td>14554.1710</td>
      <td>9.70</td>
    </tr>
    <tr>
      <th>1</th>
      <td>HONDA</td>
      <td>Red</td>
      <td>87899</td>
      <td>4</td>
      <td>$5,000.00</td>
      <td>4570.7480</td>
      <td>5.20</td>
    </tr>
    <tr>
      <th>2</th>
      <td>TOYOTA</td>
      <td>Blue</td>
      <td>32549</td>
      <td>3</td>
      <td>$7,000.00</td>
      <td>2115.6850</td>
      <td>6.50</td>
    </tr>
    <tr>
      <th>3</th>
      <td>BMW</td>
      <td>Black</td>
      <td>11179</td>
      <td>5</td>
      <td>$22,000.00</td>
      <td>497.4655</td>
      <td>4.45</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NISSAN</td>
      <td>White</td>
      <td>213095</td>
      <td>4</td>
      <td>$3,500.00</td>
      <td>7671.4200</td>
      <td>3.60</td>
    </tr>
    <tr>
      <th>5</th>
      <td>TOYOTA</td>
      <td>Green</td>
      <td>99213</td>
      <td>4</td>
      <td>$4,500.00</td>
      <td>7440.9750</td>
      <td>7.50</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HONDA</td>
      <td>Blue</td>
      <td>45698</td>
      <td>4</td>
      <td>$7,500.00</td>
      <td>3747.2360</td>
      <td>8.20</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HONDA</td>
      <td>Blue</td>
      <td>54738</td>
      <td>4</td>
      <td>$7,000.00</td>
      <td>2682.1620</td>
      <td>4.90</td>
    </tr>
    <tr>
      <th>8</th>
      <td>TOYOTA</td>
      <td>White</td>
      <td>60000</td>
      <td>4</td>
      <td>$6,250.00</td>
      <td>4680.0000</td>
      <td>7.80</td>
    </tr>
    <tr>
      <th>9</th>
      <td>NISSAN</td>
      <td>White</td>
      <td>31600</td>
      <td>4</td>
      <td>$9,700.00</td>
      <td>1049.1200</td>
      <td>3.32</td>
    </tr>
  </tbody>
</table>
</div>



# **Sampling**
## ***Get a RANDOM Fraction of the DataFrame*** 


```python

```
