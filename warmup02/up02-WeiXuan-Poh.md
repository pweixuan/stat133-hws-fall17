Warmup 02
================

``` r
knitr::opts_chunk$set(echo = TRUE)
```

``` r
github <- 'https://github.com/ucb-stat133/stat133-hws-fall17/'
repo <- 'raw/master/warmup02/data/nba2017-salary-points.RData'

download.file(
  url = paste0(github, repo),
  destfile = "nba2017-salary-points.RData")
# load the objects
load("nba2017-salary-points.RData")

# list the available objects
ls()
```

    ##  [1] "experience" "github"     "player"     "points"     "points1"   
    ##  [6] "points2"    "points3"    "position"   "repo"       "salary"    
    ## [11] "team"

``` r
class(experience)
```

    ## [1] "character"

``` r
class(github)
```

    ## [1] "character"

``` r
class(player)
```

    ## [1] "character"

``` r
class(points)
```

    ## [1] "integer"

``` r
class(points1)
```

    ## [1] "integer"

``` r
class(points2)
```

    ## [1] "integer"

``` r
class(points3)
```

    ## [1] "integer"

``` r
class(position)
```

    ## [1] "character"

``` r
class(repo)
```

    ## [1] "character"

``` r
class(salary)
```

    ## [1] "numeric"

``` r
class(team)
```

    ## [1] "factor"

Including Plots
---------------

You can also embed plots, for example:

``` r
mode(experience)
```

    ## [1] "character"

``` r
mode(github)
```

    ## [1] "character"

``` r
mode(player)
```

    ## [1] "character"

``` r
mode(points)
```

    ## [1] "numeric"

``` r
mode(points1)
```

    ## [1] "numeric"

``` r
mode(points2)
```

    ## [1] "numeric"

``` r
mode(points3)
```

    ## [1] "numeric"

``` r
mode(position)
```

    ## [1] "character"

``` r
mode(repo)
```

    ## [1] "character"

``` r
mode(salary)
```

    ## [1] "numeric"

``` r
mode(team)
```

    ## [1] "numeric"

``` r
#Testing for vectors
is.vector(experience)
```

    ## [1] TRUE

``` r
is.vector(github)
```

    ## [1] TRUE

``` r
is.vector(player)
```

    ## [1] TRUE

``` r
is.vector(points)
```

    ## [1] TRUE

``` r
is.vector(points1)
```

    ## [1] TRUE

``` r
is.vector(points2)
```

    ## [1] TRUE

``` r
is.vector(points3)
```

    ## [1] TRUE

``` r
is.vector(position)
```

    ## [1] TRUE

``` r
is.vector(repo)
```

    ## [1] TRUE

``` r
is.vector(salary)
```

    ## [1] TRUE

``` r
is.vector(team)
```

    ## [1] FALSE

``` r
is.list(experience)
```

    ## [1] FALSE

``` r
is.list(github)
```

    ## [1] FALSE

``` r
is.list(player)
```

    ## [1] FALSE

``` r
is.list(points)
```

    ## [1] FALSE

``` r
is.list(points1)
```

    ## [1] FALSE

``` r
is.list(points2)
```

    ## [1] FALSE

``` r
is.list(points3)
```

    ## [1] FALSE

``` r
is.list(position)
```

    ## [1] FALSE

``` r
is.list(repo)
```

    ## [1] FALSE

``` r
is.list(salary)
```

    ## [1] FALSE

``` r
is.list(team)
```

    ## [1] FALSE

``` r
length(experience)
```

    ## [1] 441

``` r
length(github)
```

    ## [1] 1

``` r
length(player)
```

    ## [1] 441

``` r
length(points)
```

    ## [1] 441

``` r
length(points1)
```

    ## [1] 441

``` r
length(points2)
```

    ## [1] 441

``` r
length(points3)
```

    ## [1] 441

``` r
length(position)
```

    ## [1] 441

``` r
length(repo)
```

    ## [1] 1

``` r
length(salary)
```

    ## [1] 441

``` r
length(team)
```

    ## [1] 441

Not all of them have the same length
====================================

Selected quantitative variable - salary
=======================================

Selected categorical variable - position
========================================

``` r
summary(salary)
```

    ##     Min.  1st Qu.   Median     Mean  3rd Qu.     Max. 
    ##     5145  1286160  3500000  6187014  9250000 30963450

``` r
sd(salary)
```

    ## [1] 6571890

``` r
plot(density(salary))
```

![](up02-WeiXuan-Poh_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-7-1.png)

``` r
is.factor(position)
```

    ## [1] FALSE

``` r
#False
factor(position)
```

    ##   [1] C  PF SG PG SF PG SF SG SF PF PF C  SG PG C  C  SF PG PF C  SG SG SF
    ##  [24] PG PF SG PG SF SF C  SF SG PG SG SF PG C  C  PG C  SG SF PF PF PF SF
    ##  [47] SG PG PF C  C  C  PG C  PF SF SG SG PG SF PG C  PF PG SF PF PG SF C 
    ##  [70] PF PF SF SG SF C  PF SG C  SF SG PG PF PF SG PF C  SG PG C  SF PF PG
    ##  [93] PG PF SG PF SG C  SF PF PF SG PF PG C  SG SG SG PG SF C  PG PF SF PG
    ## [116] C  SG PG C  PF PF SG SF SF PF SG PG C  SG C  C  C  PG C  SG PF PG PF
    ## [139] SG SF SG SF PG SF PF PG PG PF PF C  SG PF PG SG PF SF C  SG PG SG SF
    ## [162] PG SG PG C  SG PF C  PF C  PF SF SG SG C  SF C  PG PG SF PG SG PF SG
    ## [185] SG SF C  SG C  SF PF PF SG C  PG C  SF SG C  SF PG C  PG C  SF PF SG
    ## [208] C  SF PG PG SG C  SF PF SG SF SG PG PF SF C  C  PF SG PF C  SF C  SG
    ## [231] SF SG PG PG C  SG SG PF PF PG C  C  SG SF SG PF SG PG C  PG PG C  C 
    ## [254] SG PG PG PF SG C  SG PF SF SF SF SF SG PF PF PF PG C  C  SG SG SF C 
    ## [277] SF PG SF SG PF PG PF PG SF C  SF SF PF PG SG C  PG PF SG SF PF SF C 
    ## [300] SF PF SF PF PG PG PG C  PF SG PG PF SF C  SF PF PF C  PG SG SG SF PG
    ## [323] SG PF SF SG SG PG PF SF SF C  SF PF PF SG PG SG SF PF PG SG SG PG PF
    ## [346] PF SG C  SF C  C  SG SF C  C  SF PF SF C  PF SG SG PG C  PG SF PG C 
    ## [369] SG PG PF PF C  PF PG PF C  SF C  PG SG PG PF SG SG SG PG SG C  C  PG
    ## [392] SG SF PF PG SF C  PF SF SG C  PF C  C  PG PF SF PG SF PG SG SF SF PG
    ## [415] SG C  SG PF PF SF SF SG C  PF C  PG C  C  SG SF SG PF SG PG PF SG PF
    ## [438] PG SF PG C 
    ## Levels: C PF PG SF SG

``` r
table(position)
```

    ## position
    ##  C PF PG SF SG 
    ## 89 89 85 83 95

``` r
prop.table(table(position))
```

    ## position
    ##         C        PF        PG        SF        SG 
    ## 0.2018141 0.2018141 0.1927438 0.1882086 0.2154195

``` r
#Relatively equal with no major deviation
barplot(table(position))
```

![](up02-WeiXuan-Poh_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-8-1.png) No lists, 12 vectors Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.
