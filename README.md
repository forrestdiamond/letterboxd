
<!-- README.md is generated from README.Rmd. Please edit that file -->
letterboxd
==========

<!-- badges: start -->
<!-- badges: end -->
Let's have some fun with my letterboxd data...

Data
----

Letterboxd has several different files for data analysis. For instance, the `diary` file looks like this:

``` r
diary <- read.csv(file.path(here::here(), "data", "diary.csv"))
diary %>% 
  as_tibble() %>% 
  sample_n(5)
#> # A tibble: 5 x 8
#>   Date   Name     Year Letterboxd.URI     Rating Rewatch Tags  Watched.Date
#>   <fct>  <fct>   <int> <fct>               <dbl> <fct>   <fct> <fct>       
#> 1 2019-~ Golden~  1995 https://letterbox~    3.5 ""      ""    2019-11-20  
#> 2 2019-~ Captai~  2011 https://letterbox~    2.5 ""      ""    2019-07-07  
#> 3 2019-~ Joker    2019 https://letterbox~    3.5 ""      ""    2019-11-19  
#> 4 2019-~ Destro~  2018 https://letterbox~    3.5 ""      acti~ 2019-03-21  
#> 5 2018-~ The Ni~  2016 https://letterbox~    4   ""      budd~ 2016-08-03
```

Another useful file might be `watchlist`:

``` r
watchlist <- read.csv(file.path(here::here(), "data", "watchlist.csv"))
watchlist %>% 
  as_tibble() %>% 
  sample_n(5)
#> # A tibble: 5 x 4
#>   Date       Name          Year Letterboxd.URI                           
#>   <fct>      <fct>        <int> <fct>                                    
#> 1 2019-10-10 Baraka        1992 https://letterboxd.com/film/baraka/      
#> 2 2019-07-09 Philadelphia  1993 https://letterboxd.com/film/philadelphia/
#> 3 2018-05-09 Brick         2005 https://letterboxd.com/film/brick/       
#> 4 2018-10-13 Samurai Cop   1991 https://letterboxd.com/film/samurai-cop/ 
#> 5 2019-06-05 Luce          2019 https://letterboxd.com/film/luce/
```

You can view all available files by checking the `data/` folder.
