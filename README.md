# perpy
Functions commonly used in computer paper writing and scientific research.

## load dataset from file
```Python
import perpy as py
x = py.load()
```
![image](https://user-images.githubusercontent.com/82493254/119088330-17333200-ba3b-11eb-8b26-5909c721409e.png)
![image](https://user-images.githubusercontent.com/82493254/119088467-4e094800-ba3b-11eb-946c-048f1b496e62.png)

```Python
print(x)
```
![image](https://user-images.githubusercontent.com/82493254/119088970-0e8f2b80-ba3c-11eb-98b3-0cdeeb7b2f37.png)

### Parameters
#### path
    optional: None(**default**), string
    None: current directory,
data file directory
#### col_labels
    optional: None(**default**), number
    None: non labels,
    0: the labels is in the first column,
    otherwise: the labels is in the last column
### scaling
    optional: True(**default**), False
    True: to max min scaling,
    False: no max min scaling
### Return
    (x, labels) / x
    x: samples set
    labels: label set

## calculate the euclidean distance between point A and point B
### Function name
    dist
### Parameters
#### A
    point A
#### B
    point B
### Return
    the eudlidean distance between point A and point B

## draw scatter
### Function name
    plt_scatter
### Parameters
#### x
    samples set
#### labels
    labels set
#### axis_show
    optional: True(**default**), False
    True: show axis
    False: non axis
#### fig_label
    optional: [None](**default**), list
    [None]: non figure label
    otherwise:
      list[0] is x label
      list[1] is y label
 #### fig_legend
    optional: None(**default**),list
    None: non legend
    list: list[0] is text, 
 
    list[0] is location
      '00' is up left,
      '01' is up right,
      '10 is down left,
      '11' is down right
   
 #### save
     option: [None](**default**), list
    [None]: Do not save
     list: list[0] is file name, list[1] is dpi
 
 ## draw runtime
 ### Function name
    plt_runtime
 ### Parameters
 #### times
     y axis
 
     list[0] is 1th method time
 
    list[1] is 2th method time
 
    ...
 
    list[n-1] is n-th method time
 
 #### instances
    x axis
 
 #### save
     option: [None](**default**), list
     [None]: Do not save
     list: list[0] is file name, list[1] is dpi
 
 ## draw radar chart
 ### Function name
     plt_radar
 ### Parameters
 #### labels
    list
 
 #### data
    data list
 
 #### algorithm
     algorithm list
 
 #### title
     figure tile
 
 #### legend
    figure legend
 
 #### save
      option: [None](**default**), list
     [None]: Do not save
     list: list[0] is file name, list[1] is dpi
