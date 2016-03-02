
[<img src="https://github.com/QuantLet/Styleguide-and-FAQ/blob/master/pictures/banner.png" width="880" alt="Visit QuantNet">](http://quantlet.de/index.php?p=info)

## [<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/qloqo.png" alt="Visit QuantNet">](http://quantlet.de/) **approx** [<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/QN2.png" width="60" alt="Visit QuantNet 2.0">](http://quantlet.de/d3/ia)

```yaml

Name of Quantlet : approx

Published in : plotting

Description : Shows a loop that approximates the golden ratio and that stops at a certain point.

Keywords : proximity, sampling, iterative, approximation

Author[New] : Ludgar Evers

Submitted : Mon, November 10 2014 by Anne Israel

```


```r

# clear history
rm(list = ls(all = TRUE))
graphics.off()

x = 1                         #set initial value
for (i in 1:50) {             #repeat 
    old.x = x                 #store old value
    x     = 1 + 1/x           #update x
    if (abs(old.x-x)<10e-10)  #check for convergence
        break
}

x                             #print result
(1+sqrt(5)) / 2               #compare to desired answer

```
