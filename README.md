DevOpsLab1_ArtemBelov.ipynb - file contains Jupyter notebook with a code for webCrawler
This web Crawler is made to perform BFS (breadth-first-search) through russian wikipedia pages and collect: 
1) links (link of the page from which this page was reached, link for the current page, and concatenated links for images found on this page),
2) heading of the current page
3) concatenated sub-headings on the current page

It does so by utilizing python librarier 'requests' and 'bs4' with a 'sleep_time' variable defined before functions, used in time.sleep(sleep_time) function call to prevent too much requests being sent too frequently

output1.xlsx - is the output file with the following fields:
1) "prev_page_link" - wiki page from which current wiki page was accessed
2) "current_page_link" - link of the current wiki page
3) "heading" - heading of the wiki page
4) "sub_headings" - sub headings from the wiki page concattenated with ' ; '
5) "images" - links to images on the current wiki page concattenated with ' ; '

To run the web crawler the function wiki_crawler(path, start_url, links_lim=1000) in DevOpsLab1_ArtemBelov.ipynb should be run, where parameters are as follows:
1) 'path' - path to the output .xlsx file
2) 'start_url' - url of the wiki page to start crawler from
3) 'links_lim' - the maximum number of links to visit
