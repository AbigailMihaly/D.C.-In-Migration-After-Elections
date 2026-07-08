# D.C. Migration Flows (Lede Project 1)

This project explores the states from which people move to Washington, D.C. in different election years.

I wanted to know how much the observed "vibe shift" that happens in D.C. after an election year is related to from which states people are moving into D.C., also also their party affiliations.

Link to project:

### COMMENTARY ###

Cleaning

This is my first project ever, so everything was new. Taught myself a whole lot of pandas in order to clean these excel sheets, and then manipulate columns across the different .csvs so that I could compare across years.

The data, described more below, also comes from multiple sources, so practiced merging different data. 

Visualization

Charts: Most of this was done in datawrapper, for ease, and also ease of downloading as a .svg.
I did make some charts directly in python with matplotlib , but didn't end up using them because they exported as raster images and therefore looked bad on my website.
Maps: Learned how to make maps with plotly! AI helped me figure out how to overlap my information onto a base map of the U.S. Good stuff!

Website/publishing

I worked with Soma's basic .html template to make this into a website. I initially tried doing some scrollama stuff but in the end decided it was too complex for a first project and not worth the squeeze in terms of what I wanted to do with my project.
Biggest challenge I overcame in the .html stuff was getting multiple images or charts to format correctly side by side.

What I didn't have time for:

There are a few shortcuts I took due to time, such as basing all my per capita calculations on the 2020 population rather than each year's seperate population.

There are many angles left to explore in this project! For example, I'm very currious about there being pretty much no change to voter registrations after elections, and would like to explore why this might be, and whether there are a significant number of people living and working in D.C. that do not vote there. I would have also liked to do some interviews about the "vibe shift" in the city and what other factors may be contributing to it.

I also would have liked to experiment with the website/visualizations more.

### DATA ###

1) I downloaded my raw  data from the U.S. census, in the form of .xls sheets for each year.
That data is available here: https://www.census.gov/data/tables/time-series/demo/geographic-mobility/state-to-state-migration.html
--> a note that 2020 data not available due to COVID.
This took a fair amount of cleaning because the original format is excel files that are not continuous but rather wrap around for easier viewing on a computer but harder parsing. 

2) I also used 2020 census population data, available here:

3) D.C. voter registration information available in PDF form here: https://www.dcboe.org/data,-maps,-forms/voter-registration-statistics 
I manually pulled the information I needed into a spreadsheet titled "DC-voter-registration-data-by-year.csv"

4) Winners of each election for each state from Harvard: data source: MIT Election Data and Science Lab, 2017, "U.S. President 1976–2024", https://doi.org/10.7910/DVN/42MVDX, Harvard Dataverse, V10, UNF:6:xpBppxfswpr+u9xZe7/u7w== [fileUNF] 

###NOTEBOOKS###


Install to run the notebooks:
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import matplotlib.colors as mcolors
import plotly.express as px

may need to pip install in terminal if dont have any of the above.

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

