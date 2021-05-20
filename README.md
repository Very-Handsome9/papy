# papy
Functions commonly used in computer paper writing and scientific research.

## load dataset from file
### Function name
load
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
 optional: None(**default**),
