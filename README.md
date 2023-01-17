# Flatiron_Phase_1_Project
FlatIron Phase 1 Project - Movie Analysis
# Project Overview 
### Project Objective

Microsoft is plannning to break into the movie delevepment space via  the formulation of their own proprietary movie studio. Microsoft, like most movie companies, is looking to maximize their success at the box office from the get-go. 

In order to maximize this likely-hood of success, an analysis of the top performing movies since 2010 has been completed in order to attempt to distill a few of the factors that have contributed to their success, allowing Microsoft to use this as a framework on which to develop their own movies and hopefully mimic the success.
### Analysis Overview

In order to obtain the relevant data to determine the success and the factors that may have contributed to that for movies that have been released post 2010 two major movie databases were queried. 

#### Data Sources

The first data source was a IMDB database (IMDB.com) which contains basic information regarding 146,144 different movie titles that have been released since 2010. This database contains descriptive factors of movies such as their release data and genres as well as info on the cast and creators of said movie. This will provide our analysis with a number of different movie factors to choose from when determining why a movie may have been successful.

The second data source quiered was from the_numbers.com, a company that logs financial information regarding movies, such as the gross income and production budget. This database, though much smaller than the IMDB database, as it only contains 5,872 movies in total and 2,194 titles from 2010 and beyond, has extremely important production budget finicial information included that is a key piece of how we will determine the success of a movie.

When combining these two databases in order to form a new, complete database only of movies that contained all of the relevant information outlined below we end up with a sample size of 1,859. The limitations regarding this dataset are covered in depth later in this analysis. 

#### Determining the "Success" of a Movie

Microsoft like most companies is likely looking to maximize their profits while minimizing their investments, therefore the success metric used within this analysis to determine a movie's success will be the Return on Investment or ROI. ROI acts as a gauge of an investment's profitability, so a higher ROI means a that greater profitabilty in relation to the initail investment. For this analysis the investment metric will be the production budget of a movie and a movie's profitabilty will be determined via its worldwide gross income. The movies with the highest ROIs will be considered the most successful and we will compare the factors that make up the most successful movies to those of all of the movies in the dataset to determine what perctange of movies with a certain factor reached high levels of success.

#### Factors explored that may have contributed to a Movie's success

The culture surrounding movies is constantly in flux and has changed significantly over the past 100 years since their gain in popularity in the early 20th century. For this reason, this analysis focuses only on movies that were released after 2010, as it may be likely that the factors that contributed to the success movies released prior to that are no longer relevant in the modern world.

##### Genre

The genre of a movie tends to be the first descriptive piece used when describing a movie beyond it's title. People also tend to describe the types of movies that they enjoy most by their genre, therefore it is very possible that people choose what movies to see largely based on the genre. This analysis uses ROI and genre to find out what percentage of movies in each genre end up with a high level of success so we can therefore guide microsoft on which genres they should focus on.

##### Month Released

The movie viewing habits of the global population my change throughout the calendar year for a myriad of factors. This analysis compares the release month of movies with high levels of success with that of the larger database to determine what percentage of movies released in a given month reach high levels of success to therefore provide Microsoft with a recomendation on the time of year their movies should be released to maximize success liklihood. 

##### Production Budget

The production budget or, original investment into a movie is another very important factor in the early steps of movie development as this will guide many, if not almost all of the factors of a movie moving forward. In order to determine what Microsoft initial investment should be to maximize ROI, an analysis of different ranges of production budgets vs their success at each level was completed to give microsoft an idea of how much they should budget for each movie to maximize ROI.

## Project Limitations


Do not fully understand the origins of the databases
    How movies were selected for inclusion
    Is the info accurate?
A much larger dataset could be built beyond the limitations of the provided datasets.
This analysis does not actual measure the how any of these factors impact the results as it is only a descriptive analysis
It is possible that two movies with the same name came out in the same year
The-Numbers.com database sometimes used the “Video Release” date in place of the original release date, to compensate a tolerance of 1 year was used during the merge.
The same movie may be released at different times in different countries
Investment portion of ROI does not include all factors of interest such as advertising budget
Worldwide Gross does not contain factors such as merchandise and other peripheral sales


## Calculating the Return on Investment (ROI) 

This will be based on worldwide gross income and production cost being sourced from the tn_budgets

### General forumla to calculate ROI:

$$
ROI = \frac{\text{Net Income}}{\text{Cost of Invetment}} * 100
$$

### Formula to calculate a Movie's ROI:
$$
ROI = \frac{\text{Worldwide Gross Income}}{\text{Production Budget}} * 100
$$

## Production Budget Analysis


## Release Month Analysis
### Creating Bar Graph to show the month of release used the most for Top Movies in our dataset
In order to determine which month Microsoft should release its new movies we will look for release month trends within the movies in the present dataset with an ROI >= 500%



## Genre Analysis


