## **Almarai Stock prices**




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
      <th>Date</th>
      <th>Open</th>
      <th>High</th>
      <th>Low</th>
      <th>Close</th>
      <th>Adj Close</th>
      <th>Volume</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2020-08-23</td>
      <td>54.900002</td>
      <td>56.099998</td>
      <td>54.599998</td>
      <td>56.099998</td>
      <td>55.037498</td>
      <td>1399236</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2020-08-24</td>
      <td>56.400002</td>
      <td>56.599998</td>
      <td>55.400002</td>
      <td>55.700001</td>
      <td>54.645077</td>
      <td>2239510</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2020-08-25</td>
      <td>55.700001</td>
      <td>56.000000</td>
      <td>55.000000</td>
      <td>55.000000</td>
      <td>53.958336</td>
      <td>1285251</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2020-08-26</td>
      <td>55.000000</td>
      <td>55.500000</td>
      <td>54.500000</td>
      <td>54.599998</td>
      <td>53.565910</td>
      <td>654401</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2020-08-27</td>
      <td>54.900002</td>
      <td>55.000000</td>
      <td>54.500000</td>
      <td>54.700001</td>
      <td>53.664017</td>
      <td>541958</td>
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
    </tr>
    <tr>
      <th>246</th>
      <td>2021-08-16</td>
      <td>56.099998</td>
      <td>56.400002</td>
      <td>55.799999</td>
      <td>56.099998</td>
      <td>56.099998</td>
      <td>340565</td>
    </tr>
    <tr>
      <th>247</th>
      <td>2021-08-17</td>
      <td>55.799999</td>
      <td>56.500000</td>
      <td>55.700001</td>
      <td>56.500000</td>
      <td>56.500000</td>
      <td>284851</td>
    </tr>
    <tr>
      <th>248</th>
      <td>2021-08-18</td>
      <td>56.400002</td>
      <td>57.099998</td>
      <td>56.200001</td>
      <td>56.799999</td>
      <td>56.799999</td>
      <td>332975</td>
    </tr>
    <tr>
      <th>249</th>
      <td>2021-08-19</td>
      <td>56.500000</td>
      <td>56.500000</td>
      <td>55.900002</td>
      <td>55.900002</td>
      <td>55.900002</td>
      <td>294943</td>
    </tr>
    <tr>
      <th>250</th>
      <td>2021-08-22</td>
      <td>55.599998</td>
      <td>56.099998</td>
      <td>55.299999</td>
      <td>55.599998</td>
      <td>55.599998</td>
      <td>368605</td>
    </tr>
  </tbody>
</table>
<p>251 rows × 7 columns</p>
</div>



## **Daily Change**
### **It is the difference between a stock's current price and its price as of market close on the prior trading day**




    0     -1.199996
    1      0.700001
    2      0.700001
    3      0.400002
    4      0.200001
             ...   
    246    0.000000
    247   -0.700001
    248   -0.399997
    249    0.599998
    250    0.000000
    Length: 251, dtype: float64



## **Daily Change of the frist 10 days from the fiscal year**




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
      <th>Date</th>
      <th>Open</th>
      <th>High</th>
      <th>Low</th>
      <th>Close</th>
      <th>Adj Close</th>
      <th>Volume</th>
      <th>Daily Change</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2020-08-23</td>
      <td>54.900002</td>
      <td>56.099998</td>
      <td>54.599998</td>
      <td>56.099998</td>
      <td>55.037498</td>
      <td>1399236</td>
      <td>-1.199996</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2020-08-24</td>
      <td>56.400002</td>
      <td>56.599998</td>
      <td>55.400002</td>
      <td>55.700001</td>
      <td>54.645077</td>
      <td>2239510</td>
      <td>0.700001</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2020-08-25</td>
      <td>55.700001</td>
      <td>56.000000</td>
      <td>55.000000</td>
      <td>55.000000</td>
      <td>53.958336</td>
      <td>1285251</td>
      <td>0.700001</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2020-08-26</td>
      <td>55.000000</td>
      <td>55.500000</td>
      <td>54.500000</td>
      <td>54.599998</td>
      <td>53.565910</td>
      <td>654401</td>
      <td>0.400002</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2020-08-27</td>
      <td>54.900002</td>
      <td>55.000000</td>
      <td>54.500000</td>
      <td>54.700001</td>
      <td>53.664017</td>
      <td>541958</td>
      <td>0.200001</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2020-08-30</td>
      <td>54.400002</td>
      <td>55.200001</td>
      <td>54.000000</td>
      <td>55.200001</td>
      <td>54.154549</td>
      <td>382719</td>
      <td>-0.799999</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2020-08-31</td>
      <td>55.200001</td>
      <td>55.200001</td>
      <td>53.700001</td>
      <td>53.700001</td>
      <td>52.682957</td>
      <td>1076298</td>
      <td>1.500000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2020-09-01</td>
      <td>54.000000</td>
      <td>54.500000</td>
      <td>53.099998</td>
      <td>53.299999</td>
      <td>52.290531</td>
      <td>1136239</td>
      <td>0.700001</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2020-09-02</td>
      <td>53.700001</td>
      <td>53.700001</td>
      <td>52.900002</td>
      <td>53.299999</td>
      <td>52.290531</td>
      <td>613606</td>
      <td>0.400002</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2020-09-03</td>
      <td>53.599998</td>
      <td>54.000000</td>
      <td>53.400002</td>
      <td>54.000000</td>
      <td>52.977272</td>
      <td>595617</td>
      <td>-0.400002</td>
    </tr>
  </tbody>
</table>
</div>



## **stock daily percentage change**

    stock percentage change
    




    0      2.185785
    1     -1.241136
    2     -1.256734
    3     -0.727276
    4     -0.364301
             ...   
    246    0.000000
    247    1.254482
    248    0.709215
    249   -1.061943
    250    0.000000
    Length: 251, dtype: float64



## **Prices Charter**




    Text(0, 0.5, 'Price')




    
![svg](Almarai_Company_files/Almarai_Company_10_1.svg)
    

