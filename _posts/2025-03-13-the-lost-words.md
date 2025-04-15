---
layout: post
title:  "The Lost Words: Analysis of Book Bans"
author: lotus
description: On book bans   
image: "/assets/images/books-header.jpg"
---
# Are Book Bans Targeting a Specific Community?  
This is a question I've been grappling with recently. We hear about media bans left and right and how they skew people's perceptions of the world. Everyone holds their own beliefs about this subject, but a close confidant of mine once told me we should challenge our beliefs. That is exactly what I'm doing here—challenging what I believe to see where it leads me.

The image below shows the number of unique titles challenged by year: 

<img src="{{site.url}}/{{site.baseurl}}/assets/images/censorship-on-the-rise.jpg" alt="" style="width:450px;"/>
<img src="{{site.url}}/{{site.baseurl}}/assets/images/number-of-challenged.jpg" alt="" style="width:450px;"/>

It is evident that number of book censorships have risen exponentially over the years. The reasons could vary vastly depending on the reason of the book ban. Now that I know my research wouldn't be futile, I am ready to plunge into the waters of data!

---

## Meet the Data  
For this blog, I used the following resources:  
* <a href="https://developers.google.com/books/docs/overview" target="_blank">Google Books API</a>
* <a href="https://pen.org/book-bans/pen-america-index-of-school-book-bans-2023-2024/https://developers.google.com/books/docs/overview" target="_blank">PEN America's Index of School Book Bans (July 1, 2022 - June 30, 2023)</a> 

The second link is a csv file which I will be using to cross reference with the Google Books API to see how many books banned are LGBTQIA+ related.

I used the Google Books API key to its full potential. A few tricks I picked up along the way:  
1. Use `time.sleep(1)` between each retrieval to avoid overloading the system.  
I initially tried too download over 3000 books using the Google Books API but that turned out to be an outrageous amount and it kept halting the process. That is when I discovered the `time.sleep(1)` function which quite literally saved my code. This method made data collection time consuming but is so much more ethical as it doesn't overwhelm the API servers! Remember to be ethical as a data scientist!

(note: I used a csv file to save the data on each book (insteaed of sotring it in a variable)which immensely helped with the data collection process.)
2. Familiarize yourself with the API structure—- I've outlined this in my <a href="https://github.com/lotus-pad/blog-codes.git" target="_blank">GitHub repo</a>. Truth be told, the <a href="https://developers.google.com/books/docs/overview" target="_blank">Google Books API document</a> is not very helpful in learning how the data itself works. My code on GitHub is more detailed with comments which should be helpful incase you would ever want to replicate what I did.

I used the following url:
```
url = 'https://www.googleapis.com/books/v1/volumes'
```
Here's another code chunk from my repo regarding what parameters I used for the Google API:
```
query = f'intitle:"{title}" inauthor:"{last_name}"'

params = {
    'q': query,
    'fields': 'items(volumeInfo)',
    'key': books_key
}
```
You will find that `items(volumeInfo)` has the following variables for each observation: `['title', 'subtitle', 'authors', 'publisher', 'publishedDate', 'description', 'industryIdentifiers', 'readingModes', 'pageCount', 'printType', 'categories', 'averageRating', 'ratingsCount', 'maturityRating', 'allowAnonLogging', 'contentVersion', 'panelizationSummary', 'imageLinks', 'language', 'previewLink', 'infoLink', 'canonicalVolumeLink']`.

For simplicity, and time's sake, I used `title`, `authors`, `publishedDate`, `categories`, `description`, `maturityRating`, and `ISBN_13` from `industryIdentifiers`.


After spending over 20 hours working on this process, it’s clear that drawing conclusions on a topic like this requires even more dedication, which I hope to give in the future.

---

## Exploratory Data Analysis (EDA)  
The dataset I have focuses on 4,098 books that I retrieved by cross-matching banned books with data from the Google Books API. The *books.csv* file contains seven variables: Title, Author, Published Date, Categories, Description, ISBN_13, and Maturity Rating.  

The information I’m most interested in is the maturity rating and the description. I want to see if I can find a common thread among the banned books.

---

Take a look at the <a href="https://www.ala.org/bbooks/frequentlychallengedbooks/top10" target="_blank">Top 10 Most Challenged Books of 2023</a> by the American Library Association (ALA), and you’ll notice that most of the challenged books are LGBTQ+ related. The ALA defines "challenged" as "an attempt to remove or restrict materials, based on the objections of a person or group."

<img src="{{site.url}}/{{site.baseurl}}/assets/images/books.jpg" alt="" style="width:600px;"/>

---

## Afterthoughts  
### Why Do Book Bans Matter?  
Firstly, they affect the First Amendment right to freedom of speech. Secondly, the book industry is predominantly white—traditionally white males. This leaves underrepresented groups, such as the LGBTQ+ community, voiceless and at risk of having their stories erased. Books about them and their lives are essential for bridging gaps between communities and fostering harmony. With lost words come lost worlds. What are your opinions on book bans?

---

### For Future Exploration:  
* ALA’s Top 100 Most Challenged Books of 1990-1999  
* ALA’s Top 100 Most Challenged Books of 2000-2009  
* ALA’s Top 100 Most Challenged Books of 2010-2019

<a href="https://github.com/lotus-pad/blog-codes.git" target="_blank">GitHub link to my code</a>