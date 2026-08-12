# libminer

The goal of libminer is to provide an overview of your R library setup.
It is a toy package created as a part of a workshop and not meant for
serious use.

## Installation

You can install the development version of libminer from
[GitHub](https://github.com/) with:

``` r

# install.packages("pak")
pak::pak("jennybc/libminer")
```

## Example usage

To get a count of installed packages in each of your library locations,
optionally with the total sizes, use the
[`lib_summary()`](https://ann-ced.github.io/libminer/reference/lib_summary.md)
function:

``` r

library(libminer)
lib_summary()
#>                                                                                        Library
#> 1                               /Library/Frameworks/R.framework/Versions/4.6/Resources/library
#> 2 /private/var/folders/cl/l7qpqj_n4vb6dcrbt1w3s5zh0000gn/T/Rtmpvuo1Uo/temp_libpath166f1a4b5103
#> 3                                             /Users/annacederberg/Library/R/arm64/4.6/library
#>   n_packages
#> 1        352
#> 2          1
#> 3        103
# specify `sizes = TRUE` to calculate the total size on disk of your packages
lib_summary(sizes = TRUE)
#>                                                                                        Library
#> 1                               /Library/Frameworks/R.framework/Versions/4.6/Resources/library
#> 2 /private/var/folders/cl/l7qpqj_n4vb6dcrbt1w3s5zh0000gn/T/Rtmpvuo1Uo/temp_libpath166f1a4b5103
#> 3                                             /Users/annacederberg/Library/R/arm64/4.6/library
#>   n_packages lib_size
#> 1        352    1.29G
#> 2          1   16.64K
#> 3        103  315.37M
```
