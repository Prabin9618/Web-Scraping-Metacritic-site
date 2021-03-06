# Web Scraping Metacritic site for PC Games

### Problem Background:
Metacritic is a web site containing details about movies, games etc. in different platforms(PC, PS4, XBOX etc.). Metacritic site contains information about different PC games released till date in the order of Metascore(a score preferred by metacritic for rating, similar to IMDb). It contains information such as Title, Description, Metascore, User Score which when extracted can be used in a meaningful format.

### Objective:
To scrape metacritic site for all PC Games(~5000 available)using BeautifulSoup and requests, use User-Agents to bypass bot detection and scrape all pages(40). To extract meaningful information which will be further processed and used to build a Game Recommender System.
Shown below is the look of Metacritic site. There are 40+ pages with 100 games on each page, sorted by decreasing order of Metascore rating.

![image](https://user-images.githubusercontent.com/35566625/142235099-0122d739-4a23-4c1d-8787-280d17320114.png)

Our task is to scrape all of these pages and arrange them to form a structured and meaningful dataset with Data Dictionary as shown below.
### Domain:
Entertainment

### Data Dictionary:
Field	| Description
--- | --- 
Title | Name of the game
Description | Short description of the game
Release Date | Date released for PC
Metascore | Metacritic score
User Score | Average rating given by users

#### Please Note:
Scraping few sites are restricted and would return a 403 forbidden error as they don't allow scrapers to scrape their site. Hence, user agent should be entered in the header so that the site recognizes the scraping request to be made by human and not a bot. Metacritic site also has a similar scenario, hence, my user agent was used for extracting this data.
