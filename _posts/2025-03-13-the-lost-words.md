---
layout: post
title:  "The Lost Words: Analysis of Book Bans"
author: lotus
description: On book bans   
image: "/assets/images/books-header.jpg"
---

**Are book bans being targeted against a certain community?** This is a question I have been trying to grapple with recently. We hear about banning media left and right and how that is skewing people's perception of the world. Everyone holds their own beliefs about this subject. However, a close confidant of mine once told me that we should challenge our beliefs. That is what I'm here to do. Challenge what I believe in to see where that leads me.
 
![censorship on the rise]({{site.url}}/{{site.baseurl}}/assets/images/rise.jpg)


----
----

## Meet the Data
In this blog, I used the following resources:
* <a href="https://developers.google.com/books/docs/overview" target="_blank">Google Books API</a>
* <a href="https://pen.org/book-bans/pen-america-index-of-school-book-bans-2023-2024/" target="_blank">PEN America's Index of School Book Bans (July 1, 2022 - June 30, 2023)</a>

I managed to use the Google Books API key twice to it's full extent. A couple of tricks that I learned along the way to avoid this. Use time.sleep(1) between each retrieval. This will make sure that you are not overloading the system.

Try and familiaraize yourself with what the structure of the API looks like. I have this written out in my GitHub code which is linked below. 

After over 20 hours on working on this process, it is safe to say that conluding on a topic like this is going to require a lot more work and dedication which I hope to be able to give this in the future. 

## EDA
My current dataset highlights 4098 total books that I was able to retrieve from cross matching between banned books and getting it's information from Google Books API. The dataset *books.csv* contains sevevn variables, namely, Title	Author	Published Date	Categories	Description	ISBN_13	Maturity Rating. 

The information that I am moost interested in is the maturity rating and description. I want to see if I am able to find a common thread between banned books.

----
----

One look at <a href="https://www.ala.org/bbooks/frequentlychallengedbooks/top10" target="_blank">Top 10 Most Challenged Books of 2023</a> by the American Library Association (ALA) and you will find that most of the challenged books to be LGBTQ+ related. The term "challenged" is defined in by the ALA as "an attempt to remove or restrict materials, based upon the objections of a person or group." 

![most challenged books for 2023]({{site.url}}/{{site.baseurl}}/assets/images/books.jpg)


## After thoughts
Why do book bans matter? Firstly, the first ammendment right of freedom to speech is affected by this. Secondly, a vast majority of the book industry is white peeple-- traditionally white males. This leaves underrepresented groups such as those belonging to the LGBT+ community to be voicless and their stories at risk of being lost. Books about them and their lives are important to create bridges between communities to create harmony! With lost words come lost worlds.



###### For future:
###### * ALA's Top 100 Most Challenged Books of 1990-1999
###### * ALA's Top 100 Most Challenged Books of 2000-2009
###### * ALA's Top 100 Most Challenged Books of 2010-2019


### [GitHub link to my code](https://github.com/lotus-pad/blog-codes.git)