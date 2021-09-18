# An-adventure-in-downloading-books

The details of the codeset and plots are included in the attached Adobe Acrobat reader (.pdf) file in this repository. 
You need to download the same to view the contents. There are referrals to other contents in BLUE colour also to follow.

A Brief Introduction
======================

The tweet was about Springer releasing around 65 books related to data science and machine learning for free to download as PDFs. Following the link in his tweet, I learned that Springer has released 408 books in total, out of which 65 are related to the field of data science. The author of the blog post did a nice job of providing the links to the Springer website for each of these books. While browsing through a couple of the links, it appeared to me that the links are all well structured and it would be worth a try to write an R script to download all of the books.

My first impluse was to use the rvest package. However, I was finding it hard to scrape the page in the “Towards Data Science” website as it is probably generated using JavaScript and not a simple HTML. The Rcrawler package which appeared to have some functions which would suit my needs. While I have heard of headless browsers before, this was my first experience using one. Rcrawler itself installs PhantomJS using which one can mimic ‘visiting’ a web page using code. The LinkExtractor function from RCrawler is a nice function which gives you the internal and external links present in a page. It also provides you with some general information on the page, which was useful to extract the name of each book.

Given the well structured pages in the Springer website, it took some simple string manipulation to find a way to generate the link to the actual PDF of the book. After that, it was a simple call to the R function download.file. As a result of this exercise, I also learned two new things

    Using a regular expression to remove the last 2 characters in a string.
    The ‘wb’ mode in download.file. In my initial experiments, I was facing some issues with the downloaded pdf which got solved using this mode.

Overall, an hour of effort based on a tweet, and I learned a few things. I will most likely not have the time to read most or any of these books but at least it helped me learn some new stuff in R. Time well spent.
