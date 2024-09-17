# Serie A match predictor and web scraper
A ML match predictor model of serie A created using a random forest

## General info

This project is a match predictor based on football matches scraped from fbref.com with the related statistics for each team.
The final result shows a precision on predicting wins and losses at around 67% but a precision on draws at 33%
To create the model I used a random forest from sklearn library


## Technologies
Created with:
*  Sklearn
*  Pandas
*  Beautiful soup
*  Requests


## Project description
#### Web scraper
For the web scraper part i used beautiful soup with requests to get the links of each team for every season selected to scrape. 
In that link i found the 2 different stats table that I scraped using pandas methos read_html.
It was also implemented a user-agent rotation for the requests and a time sleep to prevent blocking from server.
At the end all of the data is saved in the csv

#### Predictor model
Data has been loaded and cleaned to train the model.
Were also calculated rolling stats for each team of the previous 3 games to give the model more detailed information.
After some data tuning and trainings the model had pretty good outcomes.
At the end the data were cleaned and joined to get the intersection of predicted outcomes and got the final result


## Requirements

```
pip install beautifulsoup4
pip install sklearn
```

