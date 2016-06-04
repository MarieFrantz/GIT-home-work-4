# bootstrap assignment 4
Marie Wallmark  
May 31, 2016  
#this is to illustrate the Central limit theorem in R markdown:

```r
n<-30
nsim<-1000
bootnorm<-numeric(nsim)
for (i in 1:nsim){
  x<-rnorm(n)
  bootnorm [i]<-median(x)
}
summary(bootnorm)
```

```
##      Min.   1st Qu.    Median      Mean   3rd Qu.      Max. 
## -0.798700 -0.145500  0.005272  0.005787  0.166500  0.636700
```

```r
hist(bootnorm)
```

![](bootstrap_clt_files/figure-html/unnamed-chunk-1-1.png)<!-- -->

```r
sd (x)
```

```
## [1] 1.04058
```

```r
#using a second sample size
n<-60
nsim<-1000
bootnorm<-numeric(nsim)
for (i in 1:nsim){
  x<-rnorm(n)
  bootnorm [i]<-median(x)
}
summary(bootnorm)
```

```
##      Min.   1st Qu.    Median      Mean   3rd Qu.      Max. 
## -0.513400 -0.104900 -0.010350 -0.005615  0.094970  0.544500
```

```r
hist(bootnorm)
```

![](bootstrap_clt_files/figure-html/unnamed-chunk-1-2.png)<!-- -->

```r
sd (x)
```

```
## [1] 0.9226315
```

```r
#exponential distribution
n<-rexp(1000,1/50)
```
