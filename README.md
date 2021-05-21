# PERPY——Functions commonly used in computer paper writing and scientific research.
## INSTALL
```Python
pip install perpy
```
## IMPORT
```Python
import perpy as py
```
## LOAD——load dataset from file
### TEST FILE——test1.txt
>**1 5 0**  
>**2 4 0**  
>**3 3 0**  
>**4 2 1**  
>**5 1 1**  
### CASE 1——Non label & No max min scaling
```Python
path = r'D:\perpy' # file directory
col_labels = None # non label
scaling = False # no max min scaling

x= py.load(path, col_labels, scaling)
```
![image](https://user-images.githubusercontent.com/82493254/119089849-5d899080-ba3d-11eb-9863-0da34fc741f4.png)

```Python
print(x)
```
![image](https://user-images.githubusercontent.com/82493254/119089890-6f6b3380-ba3d-11eb-8b97-1397267b630f.png)
### CASE 2——The labels is in the first column & To max min scaling
```Python
path = r'D:\perpy' # file directory
col_labels = 0 # the labels is in the first column
scaling = True # to max min scaling

x, r = py.load(path, col_labels, scaling)

print(x, '\n', r)
```
![image](https://user-images.githubusercontent.com/82493254/119095915-78f89980-ba45-11eb-90a4-cfbc4c14179c.png)
### CASE 3——The labels is in the last column & No max min scaling
```Python
path = r'D:\perpy' # file directory
col_labels = 2 # the labels is in the last column. non-zero number
scaling = False # no max min scaling

x, r = py.load(path, col_labels, scaling)

print(x, '\n', r)
```
![image](https://user-images.githubusercontent.com/82493254/119096315-050ac100-ba46-11eb-943c-1dba6f603e47.png)

## DIST——Calculate the euclidean distance between point A and point B
```Python
A = np.mat([1,2,3,4]) # point A
B = np.mat([4,3,2,1]) # point B

dist = py.dist(A, B)

print(dist)
```
4.47213595499958
## PLT_SCATTER——Drawing scatter plot
```Python
path = r'D:\perpy' # file directory
col_labels = 2 # the labels is in the last column. non-zero number
scaling = False # no max min scaling

x, r = py.load(path, col_labels, scaling)

py.plt_scatter(x=x, labels=r, fig_label=['X——label','Y——label'], fig_legend=['Cluster','01'])
```
![image](https://user-images.githubusercontent.com/82493254/119098644-9d09aa00-ba48-11eb-86cc-771cacee594e.png)

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
