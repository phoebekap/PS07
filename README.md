**Phoebe Kallaher** *SDS192-01*
================

## GitHub Documents

This is an R Markdown format used for publishing markdown documents to
GitHub. When you click the **Knit** button all R code chunks are run and
a markdown file (.md) suitable for publishing to GitHub is generated.

## Including Code

You can include R code in the document as follows:

``` r
View(weather)

weather_summarized <- weather %>% 
  group_by(month) %>% 
  summarize(avg_temp = mean(temp), avg_precip = mean(precip)) 
```

## Including Plots

Here is an example of a plot:

``` r
ggplot(data = weather_summarized, aes(x = month, y = avg_precip)) +
  geom_col(fill = "lightblue") +
  labs(title = "Average Precipitation on the Ground in New York City", subtitle = "Data recorded at JFK, LGA, and EWR Airports throughout 2013", x = "Month", y = "Average Precipitation (in inches)")
```

![](README_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

Note that the `echo = FALSE` parameter was added to the code chunk to
prevent printing of the R code that generated the plot.
