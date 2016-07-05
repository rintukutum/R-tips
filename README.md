# R-tips
R-tips

# Save time while subsetting big data in R

```R
big.data <- read.table(file = 'big-data.txt',
                       sep = ',',
                       header = TRUE, # if any
                       stringsAsFactors = FALSE # very important step; it will save your time a lots
                       )


```
- let say the size of above data is 22K x 2K
- we want to remove 1000 rows from 21001 to 23000

```R
# avoid
big.data <- big.data[-c(21001:23000),] # it will take more time

# try this
big.data.n <- big.data[-c(21001:23000),]
rm(big.data)
```

