# meb2309HW1updated

My Solution to HW1

```{r}
library (tidyverse)
```
## Problem 1

```{r}
prob1_df=
  tibble(
    samp = rnorm(10),
    samp_gt_0 = samp > 0,
    char_vec = c("a", "b", "c", "d", "e", "f", "g", "h","i", "j"),
    factor_vec = factor(c("low", "low", "low", "mod", "mod", "mod", "mod", "high", "high", "high"))
)
```
Taking the mean of each variable 
```{r}
mean(pull(prob1_df, samp))
mean(pull(prob1_df, samp_gt_0))
mean(pull(prob1_df, char_vec))
mean(pull(prob1_df, factor_vec))
```
I can take the means of logical numbers and logical, however, I cannot take the mean of character or factor.

```{r}
as.numeric(pull(prob1_df, samp))
as.numeric(pull(prob1_df, samp_gt_0))
as.numeric(pull(prob1_df, char_vec))
as.numeric(pull(prob1_df, factor_vec))
```

```{r}
as.numeric(pull(prob1_df, samp_gt_0)) * (pull(prob1_df, samp))
```

## Problem 2

install.packages("palmerpenguins")

data("penguins", package = "palmerpenguins")

important variables in the penguins data set include species, island, bill_length_mm, bill_depth_mm, flipper_length_mm, body_mass_g, sex, year 

nrow (penguins)
ncol (penguins)
There are 344 rows and 8 columns in my dataset

`r mean(flipper_length_mm)`

mean(x, trim = 0, na.rm=TRUE)

```{r}
as.numeric(pull(penguins, flipper_length_mm))
```
   p <- ggplot(penguins, aes(bill_length_mm, flipper_length_mm))
   p+geom_point(aes(color=species))
   
   


The mean is `r mean(flipper_length_mm)`.