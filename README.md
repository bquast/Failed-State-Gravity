Failed State Gravity Model
====================================
Bastiaan Quast and Daniel Norfolk
------------------------------------

Abstract
------------------------------------
An application of the gravity model to the interactions of failed states.

An example - Afganistan and Pakistan
------------------------------------
As an example, let us estimate this for Afganistan Pakistan using the failed state index for 2013 and the distance between Karachi and Kabul.




```r
Afg = 106.7
Pak = 102.9
distAP = 1091.76
```


The FSI should be normalised using z-scores.


```r
mean = 70.5
stDev = 23.5
AfgZ <- (Afg - mean)/stDev
PakZ <- (Pak - mean)/stDev
AfgZ
```

```
## [1] 1.54
```

```r
PakZ
```

```
## [1] 1.379
```


Now we estimate the index:


```r
IndAP <- (AfgZ * PakZ)/distAP
IndAP
```

```
## [1] 0.001945
```


A comparison, Finland and Sweden
--------------------------------
Input the data


```r
Fin = 18
Swe = 19.7
distFS = 1091.76
```


The FSI should be normalised using z-scores.


```r
FinZ <- (Fin - mean)/stDev
SweZ <- (Swe - mean)/stDev
FinZ
```

```
## [1] -2.234
```

```r
SweZ
```

```
## [1] -2.162
```


Estimate the index

```r
IndFS <- (FinZ * SweZ)/distFS
IndFS
```

```
## [1] 0.004423
```

