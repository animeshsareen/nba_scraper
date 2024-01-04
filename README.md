# nba_scraper
Input a player's name and get years of their NBA stats as a pandas df.

## purpose
- This tool helps sports fans use data science to beat sportsbooks.
- It extracts any active NBA player's game logs into a df (2019-now).
- The tool also has en etl() function to clean this data for visualization via Plotly.
## tools used
- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical operations.
- `requests`: For sending HTTP requests to websites.
- `beautifulsoup`: For parsing HTML and extracting data.
- `matplotlib`: For creating static, interactive, and animated visualizations.
- `plotly`: For creating interactive and aesthetically pleasing visualizations.
- `ipywidgets`: For creating interactive UI elements in Jupyter notebooks.
## scraper
``` python
curry = collect('stephen curry')
```
This creates a dataframe `curry` with Curry's original stats.

## etl
``` python
df = etl(curry)
```
This simply stores Curry's cleaned data in a new `df`. 

## plotting interactive stats
This function creates an interactive scatterplot of your player's performance in any given statistic, using color as a third dimension to encode opponents in the visual.
``` python
stat = '3p'
line = 6

scatter(df, stat, line)
```
You can click on any team to isolate those points, scope in and out by dragging.
There's also a handy tool bar in the top right.

<img width="1314" alt="zoom" src="https://github.com/animeshsareen/nba_scraper/assets/119532344/405fc713-869a-4c0e-8400-cc16e92b923b">

### more interactive plots
This one plots a bar graph of your chosen stat's average per game (ppg, rebpg, etc.) against each opponent.
``` python
# xpg usage
xpg(df)
```
I chose #7 (3pa).

<img width="1358" alt="xpg" src="https://github.com/animeshsareen/nba_scraper/assets/119532344/e52c181c-f9dc-4d1c-9500-e498e96a3f38">

Have fun!

---
## license

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

MIT License grants users broad permissions to modify and distribute the software, provided that all copies include the original copyright and license notice. This encourages open source collaboration and sharing, as users can adapt the project for their own needs and contribute improvements to the community.

