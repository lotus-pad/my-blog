---
layout: post
title:  "The Lost Words: Analysis of Book Bans using Streamlit"
author: lotus
description: On book bans and EDA using streamlit  
image: "/assets/images/books-header.jpg"
---

# Why are so many books being banned—and who’s most affected?

Lately, I’ve been thinking a lot about book censorship. It’s a topic that’s become increasingly concerning, and over the past few years, there’s been a noticeable spike in the number of books being challenged or outright removed from libraries and classrooms.

In a previous post, I did some light EDA and data collection to dig into this trend:  
📜 <a href="https://lotus-pad.github.io/my-blog/2025/04/15/the-lost-words.html" target="_blank">The Lost Words: Analysis of Book Bans</a>

Here's the gist of it:

**Are LGBTQIA+ stories and authors being targeted more than others?**  
That was the big question I wanted to explore.

Over the past decade, the number of banned or challenged books has *dramatically* increased—and the visuals speak for themselves:

<img src="{{site.url}}/{{site.baseurl}}/assets/images/censorship-on-the-rise.jpg" alt="" style="width:450px;"/>
<img src="{{site.url}}/{{site.baseurl}}/assets/images/number-of-challenged.jpg" alt="" style="width:450px;"/>

🏷️ *Quick caveat:* I only looked at **unique books** that were banned—not how many times each book was banned across locations. That’s something I’d love to dive into next time!

---

# Meet my Streamlit App! 📮
Wanna explore the data yourself? I built a little [Streamlit app](https://the-lost-words.streamlit.app) that lets you play with the dataset I curated. Go ahead, click around!

Now you might be wondering:  
**“What can I actually do with this app?”**  
Glad you asked! Here's a quick tour:

### 1. **Filter by Author or Category**
Use the sidebar to filter the dataset by a specific author or one (or more!) categories. This is a great way to explore patterns around who's being targeted and what kinds of stories are under fire.

### 2. **Explore Filtered Books**
Check out the **"explore books"** tab to see a table of filtered results based on your selections. You can even peek at the raw, unfiltered dataset if you're feeling extra curious.

### 3. **View Summary Stats**
Head over to the **"summary stats"** tab to see a bar chart showing the top 10 most common categories of banned books. Spoiler alert: it's a bit disheartening.

### 4. **Search by Title or Description**
Wondering if a specific book or keyword has been flagged? Use the **search bar** to find titles or descriptions containing the terms you care about.

---

✒️ At the end of the day, staying informed matters.  
I hope this tool gives you a small but meaningful way to engage with this issue—and maybe even spark some conversations.

Wishing you a colorful day full of sunshine and rainbows. 🌈✨

---

# Afterthoughts

I genuinely believe that data science can be a tool for social justice—and I want to be part of that movement.

💭 What are *your* thoughts on book bans? What should we explore next?

---

### For future exploration:
- Look at how many times each book has been banned
- Map bans geographically
- Track changes in author demographics over time
- Sentiment analysis of book descriptions
