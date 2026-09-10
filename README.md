# D.C. Migration Flows (Lede Project 1)

This project, compleated as part of my work for the Columbia J School's Lede Program, explores the states from which people move to Washington, D.C. in different election years.

I wanted to know how much the observed "vibe shift" that happens in D.C. after an election year is related to from which states people are moving into D.C., and who those states voted for.

## DATA

1) I downloaded my raw  data from the U.S. census, in the form of .xls sheets for each year.
That data is available here: https://www.census.gov/data/tables/time-series/demo/geographic-mobility/state-to-state-migration.html
--> a note that 2020 data not available due to COVID.

2) D.C. voter registration information available in PDF form here: https://www.dcboe.org/data,-maps,-forms/voter-registration-statistics. I collected data from end of November from year, to reflect post-election registrations.
I manually pulled the information I needed into a spreadsheet titled "DC-voter-registration-data-by-year.csv"

3) Winners of each election for each state from Harvard: data source: MIT Election Data and Science Lab, 2017, "U.S. President 1976–2024", https://doi.org/10.7910/DVN/42MVDX, Harvard Dataverse, V10, UNF:6:xpBppxfswpr+u9xZe7/u7w== [fileUNF] 

4) I also used U.S. Census data for 2020 by state, in order to calculate per capita figures.


## COMMENTARY

### Data Cleaning

I worked with U.S. census data, spending substantial time in python cleaning the sheets with pandas. One issue I encountered was that the excel spreadsheet had a wrap around format, in which the same information was repeated multiple times across the spreadsheet for different states. The excel spreadsheet appeared to be formatted that way to increase readability -- the whole of the dataset was viewable in a single computer screen without scrolling -- but it made for a complex cleaning process. I also practiced working with many excel sheets at once, as each year had its own sheet. 

### Visualization

Charts: I created the projects' charts in Datawrapper and Flourish. I did make some charts directly in python with matplotlib, but didn't end up using them because they exported as raster images and looked bad on my website. Datawrapper also provided many more customization options.

Maps: For this project, I learned how to make maps with plotly! AI helped me figure out how to overlap my information onto a base map of the U.S. Good stuff!

Website/publishing: I worked with [Soma's basic .html template](https://jsoma.github.io/page-templates/) to make this into a website.

## Future Improvements

What I didn't have time for: There are a few shortcuts I took due to time, such as basing all my per capita calculations on the 2020 population rather than each year's seperate population.

There are many angles left to explore in this project! For example, I'm very currious about there being pretty much no change to voter registrations after elections, and would like to explore why this might be, and whether there are a significant number of people living and working in D.C. that do not vote there. I would have also liked to do some interviews about the "vibe shift" in the city and what other factors may be contributing to it.

### NOTEBOOKS

Install to run the notebooks:

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import matplotlib.colors as mcolors
import plotly.express as px

May need to pip install in terminal if dont have any of the above.

A guide to each notebook

Cleaning notebooks:
- For bulk of the cleaning, beginning with state-to-state migration excel sheets for each census year.
Notebooks titled DC-migration-[YEAR]-ran.ipynb
- elections-data-cleanup.ipynb cleaned up data on winner for each state election year

Analysis notebooks:
- DC-migration-eachyear-charts.ipynb explores the data and then makes various maps and charts for inidividual data years. This is the bulk of my analysis.
- DC-migration-comparative-betweenyear-charts.ipynb explores the data and makes charts across multiple years.
- migration_total_background_calucations.ipynb looks at how D.C. stacks up to other states overall in terms of inmigration. Mostly for narrative part of the story.
- DC-migration-comparative-betweenyear-charts.ipynb
- DC-micration-data-compiled.ipynb compiles the years into one .csv. Didn't use this much for the story.

###

