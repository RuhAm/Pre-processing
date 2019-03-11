# Pre-processing
Author:MD Ruhul Amin
#Pre-processing steps:
-Read dataset
-find out missing values
Here, there is no missing values.
-find out data types
Here, all of data are in numerical form except 3 features (proto, service and state). 
-Encoding 
Here, One hot encoding is used which transforms categorical features into numerical. At first it does label encoding. 
label encoding example: 
    fruits
    Apple
    Orange
    Grape
Here in fruit column , there are 3 categories. Label encoder simple encode into 1,2,3. 
Label encoder:
    fruits
    1
    2
    3
BUt , this creates ranking and is not useful so one hot encoding is applied after this step.
One hot encoding:
    1: 0 0 1
    2: 0 1 0
    3: 1 0 0 
It adds more column and is seen as:
    fruit_grape fruit_orange fruit_apple
    0                 0           1
    0                 1           0
    1                 0           0
here, one fruit category column is changed into 3 columns by one hot encoding.
NUmber of new columns depend on unique category in each column.
In this case, there are 131,7,13 unique category in proto, state, service. 
Therefore, after one hot encoding, our feature size increased. 
We can further use feature dimension reduction techniques to extract important features. 

-FInally, correlation between features is shown in form of heatmap.
