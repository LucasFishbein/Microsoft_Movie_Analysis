# Microsoft Movie Analysis

### Getting Started with this Repository 
A Descriptive Analysis of multiple factors that may contribute to a movie's success in order apply those success factors to future movies the Microsoft will produce.
To Run this code, download the following data files from the link below and place both files in a folder you will create named "/Data" (case-sensitive) inside this repository.

Download: tn.movie_budgets.csv.gz and im.db.zip From: https://github.com/LayFish21/dsc-phase-1-project-v2-4/tree/master/zippedData
    


# Project Overview 

### Project Objective

Microsoft is planning to break into the movie development space via  the formulation of their own proprietary movie studio. Microsoft, like most movie companies, is looking to maximize their success at the box office from the get-go. 

In order to maximize this likely-hood of success, an analysis of the top performing movies since 2010 has been completed in order to attempt to distill a few of the factors that have contributed to their success, allowing Microsoft to use this as a framework on which to develop their own movies and hopefully mimic the success.

### Analysis Overview

In order to obtain the relevant data to determine the success and the factors that may have contributed to that success for movies that have been released post 2010 from two major movie databases were queried. 

## Data Sources

The first data source was a IMDB database (IMDB.com) which contains basic information regarding 146,144 different movie titles that have been released since 2010. This database contains descriptive factors of movies such as their release data and genres as well as info on the cast and creators of said movie.

The second data source queried was from the_numbers.com, a company that logs financial information regarding movies, such as the gross income and production budget. This database contains 2,194 titles from 2010 and beyond, has extremely important production budget financial information included that is a key piece of how we will determine the success of a movie.

When combining these two databases in order to form a new complete database only of movies released after 2009 that contained all of the relevant information outlined below, we end up with a sample size of 1,859. The limitations regarding this dataset are covered in depth later in this analysis. 

## Determining the "Success" of a Movie

In order to maximize profits while minimizing investments, the success metric used within this analysis to determine a movie's success will be the Return on Investment or ROI. ROI acts as a gauge of an investment's profitability, so a higher ROI means a that greater profitability in relation to the initial investment. For this analysis the investment metric will be the production budget of a movie and a movie's profitability will be determined via its worldwide gross income. 

The movies with an ROI greater than or equal to 500% will be considered "Highly Successful" and will be included in the Top Movies dataset. 

## Data Analysis

### Calculating the Return on Investment (ROI) 

As discussed above ROI will be our success metric with "high success" being an ROI >= 500%

ROI will be derived from the worldwide gross income and production cost being sourced from the tn_budgets

#### General formula to calculate ROI:

$$
ROI = \frac{\text{Net Income}}{\text{Cost of Investment}} * 100
$$

#### Formula to calculate a Movie's ROI:
$$
ROI = \frac{\text{Worldwide Gross Income}}{\text{Production Budget}} * 100
$$
The culture surrounding movies is constantly in flux and has changed significantly over the past 100 years since their gain in popularity in the early 20th century. For this reason, this analysis focuses only on movies that were released after 2010, as it may be likely that the factors that contributed to the success movies released prior to that are no longer relevant in the modern world.

##### Genre

This analysis uses ROI and genre to find out what percentage of movies in each genre end up with a high level of success so we can therefore guide microsoft on which genres they should focus on.

<img width="473" alt="Screenshot 2023-01-23 at 2 30 06 PM" src="https://user-images.githubusercontent.com/117129342/214132602-94760c96-4183-455c-96fa-70d04d6c7647.png">

##### Month Released

This analysis compares the release month of movies with high levels of success with that of the larger database to determine what percentage of movies released in a given month reach high levels of success in order to understand which release month is most likely to maximize success. 

<img width="427" alt="Screenshot 2023-01-23 at 2 29 58 PM" src="https://user-images.githubusercontent.com/117129342/214132612-ebba2ddd-85c0-4b14-9388-1c6f37bd7a2c.png">

##### Production Budget

In order to determine what Microsoft's initial investment should be to maximize ROI, an analysis of different ranges of production budgets vs their rate of success at each level was completed to give Microsoft an idea of how much they should budget for each movie to maximize ROI.

The graph below breaks the production budgets into multiple bins as described on the x-axis and shows the percent of movies in our database at that budget point that became highly successful

<img width="617" alt="Screenshot 2023-01-23 at 2 32 28 PM" src="https://user-images.githubusercontent.com/117129342/214132577-b68651ba-08cf-44f0-84e0-45d4346bb517.png">


## Project Limitations


- Did not fully understand the origins of the databases. How movies were selected for inclusion? Is the info accurate?
- A much larger dataset could be built beyond the limitations of the provided datasets.
- This analysis does not actual measure the how any of these factors impact the results as it is only a descriptive analysis
- It is possible that two movies with the same name came out in the same year
- The-Numbers.com database sometimes used the “Video Release” date in place of the original release date which caused issus when merging the two source databases, to compensate a tolerance of 1 year was used during the merge.
- The same movie may be released at different times in different countries which could create issues when the databases used were merged
- Investment portion of ROI does not include all factors of interest such as advertising budget
- Worldwide Gross does not contain factors such as merchandise and other peripheral sales


# Conclusions 

### The factors to include based on this analysis to maximize the chance of an ROI >= 500%:
Production Budget:
- Between One and Ten Million Dollars were top performer. 
- Avoid Thirty to One Hundred Million dollar range

Genre:
- Mystery and Horror were top performers. 
- Avoid War, Sport & Western

Release Month:
- June and July  were top performers. 
- Avoid December

# Next Steps

### The next steps to further investigate the task at hand is to address the limitations of this study in the following ways
**Data sources and database Size:** 
- Find a much larger database to use as the dataset for this analysis as 1859 movies may not be large enough to get reproducible results
- Be sure to fully understand how a database was formed and what the inclusion criteria for the database is

**Form a more complete picture of a movie's investment for ROI calculation:** 
- Find a database that includes other investment costs associated with a movie success such as the advertising budget and intellectual property licensing fees

**For a more complete picture of a movie's gross income for ROI calculation:**
- Find a database that includes other income sources beyond just the box office worldwide gross associated with a movie's income such as merchandise sales, intellectual property licensing fees, and post movie theater sales

## For More Information

See the full analysis in the [Jupyter Notebook](./microsoft_movie_analysis.ipynb) or review this [presentation](./Microsoft_Movie_Analysis.pdf).

For additional info, contact Lucas Fishbein at [FishbeinLucas@gmail.com](mailto:FishbeinLucas@gmail.com)


## Repository Structure

```
├── .gitignore
├── README.md
├── Microsoft_Movie_Analysis.pdf
└── Microsoft_Movie_Analysis.ipynb
```
