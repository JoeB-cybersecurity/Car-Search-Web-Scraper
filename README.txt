(FIXED! Woohoo!) This is my car search web scraper project, built using the java language and jsoup module. Limitations of this project include not working on pages that load using javascript. There are 3 files including:

-Central_Marketplace_Project: Scrapes listings on ebay, carsales and gumtree specified by user input. Only searches for cars and vehicles. Returns the title, price, URL link and img link for each individual result it finds, as well as the site it found the listing on. Can sort these results by lowest or by best match. 

This file works by manipulating the URL that the page uses to load results and scraping elements of HTML (such as href, scr, labels ect.) into one big array list. Can also modify how many pages the program will scrape from (number of items to be included in search), location, sort method and whether to include buyitnow or auction listings. After scraping the selected HTML elements, it fills a 3 dimensional (Items) and 2 dimensional array (PriceDouble), and sorts these elements into 2 dimensional (sorted items) and 1 dimensional array (itemPrice).


-ebayStats.java: Scrapes listings on ebay specified by user input. Returns the title, price, URL link and img link for each individual result it finds. It also returns the average listing price, and the highest and lowest price.


-jsoup_JS_Test: Test file for "Attempt to connect and load a HTML page using javascript. EXCEPTION END Error followed by incomplete html page". Currently only returns listing prices and total listings found on one page of a pre-set ebay search result. 


Fixes required: 
This program could use a lot of optimisation and fixes including but not limited to
-Some queries don't work as well as others? (eg. ford falcon has stringIndexOutOfBoundsException vs honda civic which works perfectly) - Caused by improper string concatination of the URL for carsales. Quick fix is to set pagesIdx = 1
-Sorting might contain some errors for formatted item price 
-Using functions to organise and replaced reused code 
-Using a better method to store items in arrays. Such as removing some arrays that arn't needed, consolidating arrays or exporting to external csv or file
-Removing unused/commented out code
-Workaround dynamic page loading (such as gumtree using "hidden" tags) 
-Workaround on pages that load using javascript
