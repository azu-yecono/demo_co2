library(tidyverse)

data <- read.csv("data/owid-co2-data.csv")
#install.packages("tidyverse")

data$gdp_per_capita <- data$gdp / data$population

data |> 
  dplyr::filter(
    year < 2016 & year > 1819 &
    country == c("United States", "Japan"))|>
  ggplot2::ggplot(
    mapping=aes(x=gdp_per_capita,
                y=co2_per_capita,
                color = factor(country)),
    group_by(country))+
  geom_point()
plot