# BP.gg Web Scraping

## Overview of Analysis

Founded in 2018 by Activision, The Call of Duty League (CDL) is the premier professional esports league for Activision's own video game series, Call of Duty. Similar to all other sports, countless player, team, and match datapoints are produced through competition. In years past, the CDL offered a public API that allowed users to conveniently access this data for analysis. However, for the 2023 season, this API has been removed, thus making gathering CDL match data significantly more difficult. Fortunately, the website breakingpoint.gg records a majority of the match data and makes the data public on its website. To organize all of the match data into a single, tidy dataset, I created `Web_Scrape.ipynb` which allows the user to scrape the breakingpoint.gg for CDL match data within any date range of the user's choosing. Once scraped, the data is converted to a Pandas DataFrame and exported to a SQL database for storage and future analysis. This program utilizes the Selenium and Splinter libraries to automatically navigate the webpages on the breakingpoint website, the Beautfiul Soup 4 (bs4) library to extract data from within the webpages' HTML files, and the SQLalchemy library to export our dataset directly to our SQL database.

## Results

![CDL DF]()

For our analysis, we scraped all CDL match data for the current season, which began December 8th, 2023. As you can see in the image above, our dataset containts 2,440 entries, where each entry corresponds to a single player's performance during a single map of a single match from the 2023 season. Each entry also contains the corresponding map and match results, as well as the date of the match, match ID, and player's team. All in all, our mission to gather CDL data into one tidy dataset was a success, thanks to our program and breakingpoint.gg.
