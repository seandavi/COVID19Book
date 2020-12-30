# Available datasets

## Searchable dataset catalog

Use the searchable, sortable table below to find datasets of interest
based on criteria in the table. To then access and get the dataset in 
R, use the `accessor` column as a function. For example, `google_mobility_data()` 
will return all currently available Google mobility. For more details
about a dataset, see the next section or type `?<accessor>`, replacing `<accessor>` 
by the value in the `accessor` column. 


```r
library(DT)
library(sars2pack)
```





```r
ad = available_datasets()
ad$url = sprintf('<a href="%s">[LINK]</a>', ad$url)
datatable(ad, escape = which(colnames(ad)=='url'))
```

![](datasets_files/figure-latex/unnamed-chunk-2-1.pdf)<!-- --> 

## Dataset details

We track relatively updated details of each dataset in the package. These 
numbers will likely be a few days out-of-date (see the `eval-date` entry below)
and will not refresh after installed.
For the most recent details, simply collect the metrics after accessing
the dataset. Information tracked here about datasets includes:

- Column names
- Column types
- Dimensions (rows X columns)
- For datasets that are time series, the first and last date included

Click the triangles in the table below to expand any dataset of interest.



```r
dd = dataset_details()
library(listviewer)
listviewer::jsonedit(dd)
```

![](datasets_files/figure-latex/unnamed-chunk-3-1.pdf)<!-- --> 
