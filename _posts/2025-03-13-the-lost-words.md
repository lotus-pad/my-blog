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

<img src="{{site.url}}/{{site.baseurl}}/assets/images/censorship-on-the-rise.jpg" alt="" style="width:600px;"/>
<img src="{{site.url}}/{{site.baseurl}}/assets/images/number-of-challenged.jpg" alt="" style="width:600px;"/>

It is evident that number of book censorships have risen exponentially.

---

## Meet the Data  
For this blog, I used the following resources:  
* <a href="https://developers.google.com/books/docs/overview" target="_blank">Google Books API</a>
* <a href="https://pen.org/book-bans/pen-america-index-of-school-book-bans-2023-2024/https://developers.google.com/books/docs/overview" target="_blank">PEN America's Index of School Book Bans (July 1, 2022 - June 30, 2023)</a> 

I used the Google Books API key to its full potential. A few tricks I picked up along the way:  
1. Use `time.sleep(1)` between each retrieval to avoid overloading the system.  
2. Familiarize yourself with the API structure—I've outlined this in my GitHub code, which is linked below.

After spending over 20 hours working on this process, it’s clear that drawing conclusions on a topic like this requires even more dedication, which I hope to give in the future.

---

## Exploratory Data Analysis (EDA)  
The dataset I have focuses on 4,098 books that I retrieved by cross-matching banned books with data from the Google Books API. The *books.csv* file contains seven variables: Title, Author, Published Date, Categories, Description, ISBN_13, and Maturity Rating.  

The information I’m most interested in is the maturity rating and the description. I want to see if I can find a common thread among the banned books.

---

Take a look at the [Top 10 Most Challenged Books of 2023](https://www.ala.org/bbooks/frequentlychallengedbooks/top10) by the American Library Association (ALA), and you’ll notice that most of the challenged books are LGBTQ+ related. The ALA defines "challenged" as "an attempt to remove or restrict materials, based on the objections of a person or group."

<img src="{{site.url}}/{{site.baseurl}}/assets/images/books.jpg" alt="" style="width:600px;"/>

---

## Afterthoughts  
### Why Do Book Bans Matter?  
Firstly, they affect the First Amendment right to freedom of speech. Secondly, the book industry is predominantly white—traditionally white males. This leaves underrepresented groups, such as the LGBTQ+ community, voiceless and at risk of having their stories erased. Books about them and their lives are essential for bridging gaps between communities and fostering harmony. With lost words come lost worlds.

---

### For Future Exploration:  
* ALA’s Top 100 Most Challenged Books of 1990-1999  
* ALA’s Top 100 Most Challenged Books of 2000-2009  
* ALA’s Top 100 Most Challenged Books of 2010-2019

[GitHub link to my code](https://github.com/lotus-pad/blog-codes.git)
