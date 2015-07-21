---
layout: page
subheadline: "Investigating Foreign Films in US Markets"
title: "Crouching Tiger, Hidden Data (Part I: Web Scraping)"
author: Trisha
teaser: "The first step in answering any question involves getting some data. In this case, that meant web scraping."
---

**All of the code from this post can be found on my [github repo](https://github.com/trishaandrews/movie_analysis), specifically in the `scrape_mojo.py` file.**  
For my second project at Metis, I wanted to predict the success of foreign movies in the US market by looking at factors such as country of origin, genre, opening theaters, etc. That turned out to be much easier said than done, but I'll get into that later. 

Anyway, after deciding what I wanted to look at, I found that the website [BoxOfficeMojo](http://www.boxofficemojo.com/), which shall henceforth be referred to as bomojo, had a handy list of [foreign language films](http://www.boxofficemojo.com/genres/chart/?id=foreign.htm). This seemed pretty perfect, especially since I was unable to find such a list on IMDB or any other easily accessible website. (Netflix has such a genre, but attempting to scrape Netflix seemed like biting off more than I could chew as a newbie web scraper, and I don't want to lose my Netflix account. Though if I wanted to get better results in the future, getting access to Netflix data would probably be necessary)  

For the actual web scraping, I used python and BeautifulSoup to locate the table in the foreign language page that contained all of the movie titles/links and country of origin, where applicable. These were saved in a dictionary of '(title, link)' keys and values of origin country or None, if the country was missing from that bomojo page. I then saved the resulting dictionary as a pickle on my local machine.

Once I had all the titles and links, it was time to scrape my data from the actual bomojo pages. Mostly this included a lot of trial and error, since, probably as a deterrent to rogue web scrapers, bomojo doesn't seem to add ids to their HTML classes. So, web scraping this site mostly was a matter of making sure I was looking at the correct table.
