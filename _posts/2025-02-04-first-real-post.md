---
layout: post
title:  "Top 5 Python Libraries for Data Science Students"
author: Lotus Khoteja
image: assets/img/dark-lotus-header.jpg
date: 2025-02-04
categories: [blog, personal]
tags: [blogging, python, python_libraries]
---

<p class="intro"><span class="dropcap">A</span>re you trying to learn a new programming language? Are you overwhelmed by all the information that is out there? You're not alone! Learning Python, like any other skill, can be daunting, but this is where everyone starts. Help is on the way! Let's take one step at a time and look at some of my favorite (and most used) Python libraries. These libraries are ranked based on their usability, beginner-friendliness, versatility, and popularity among the data science community. </p>

Each library will be rated on a scale of 1 to 5 based on the following criteria:

* **Usability**: How often I’ve used it in the last 6 months.
* **Beginner-friendliness**: How easy it is for beginners to learn and use.
* **Versatility**: How many different tasks it can handle.

Extra ranking:
* **Ranking on GeeksforGeeks**: Its popularity and relevance in the data science community.

Let’s dive in!

### Quick Summary

| Python Library  | Usability |Beginner-friendliness |Versatility | Ranking on GeeksforGeeks |
| --------------- | --------- |--------------------- |----------- | ------------------------ |
| NumPy           | 5/5       |5/5                   | 4/5        |           1              |
| Pandas          | 5/5       |4.5/5                 | 4/5        |           2              |
| Matplotlib      | 5/5       |4/5                   | 5/5        |           3              |
| SciPy           | 4/5       |4/5                   | 4/5        |           16             |
| Seaborn         | 3.5/5     |5/5                   | 4/5        |           9              | 



### 1. NumPy
**What it does**: Handles large sets of numbers efficiently, great for math and data science.  
**Example**:Creating an array and finding the average:
{%- highlight python -%}
import numpy as np
arr = np.array([1, 2, 3, 4, 5])
print(np.mean(arr))  # Output: 3.0
{%- endhighlight -%}
* **Usability**: 5/5
* **Beginner-friendliness**: 5/5
* **Versatility**: 4/5
* **[Ranking on GeeksforGeeks](https://www.geeksforgeeks.org/python-libraries-to-know/#1-numpy)**: 1

### 2. Pandas
**What it does**: Works with tables of data (like spreadsheets), making it easy to manipulate.  
**Example**: Creating a simple table:
{%- highlight python -%}
import pandas as pd
data = {'Name': ['Alice', 'Bob'], 'Age': [25, 30]}
df = pd.DataFrame(data)
print(df)
#=> Output:     
Name  Age
0  Alice   25
1    Bob   30
{%- endhighlight -%}
* **Usability**: 5/5
* **Beginner-friendliness**: 4.5/5
* **Versatility**: 4/5
* **[Ranking on GeeksforGeeks](https://www.geeksforgeeks.org/python-libraries-to-know/#2-pandas)**: 2

### 3. Matplotlib
**What it does**: Makes graphs and charts for data visualization.  
**Example**: Creating a simple line chart:
{%- highlight python -%}
import matplotlib.pyplot as plt
years = [2010, 2011, 2012, 2013, 2014, 2015, 2016, 2017, 2018, 2019, 2020]
temperatures = [14.5, 14.6, 14.6, 14.7, 14.8, 14.9, 15.0, 15.1, 15.1, 15.2, 15.3]
plt.plot(years, temperatures)
plt.xlabel('Year')
plt.ylabel('Average Global Temperature (°C)')
plt.title('Average Global Temperatures (2010-2020)')
plt.show()
{%- endhighlight -%}

Output:
<figure>
	<img src="{{site.url}}/{{site.baseurl}}/testing-code/matplotlib-eg(0).png" alt=""> 
	<figcaption>Output: Matplotlib Example</figcaption>
</figure>

* **Usability**: 5/5
* **Beginner-friendliness**: 4/5
* **Versatility**: 5/5
* **[Ranking on GeeksforGeeks](https://www.geeksforgeeks.org/python-libraries-to-know/#3-matplotlib)**: 3

### 4. SciPy
**What it does**: Builds on NumPy, adding advanced math, science, and engineering functions.  
**Example**: Finding the square root using SciPy:
{%- highlight python -%}
from scipy import sqrt
print(sqrt(16))  
#=> Output: 4.0
{%- endhighlight -%}
* **Usability**: 4/5
* **Beginner-friendliness**: 4/5
* **Versatility**: 4/5
* **[Ranking on GeeksforGeeks](https://www.geeksforgeeks.org/python-libraries-to-know/#16-scipy)**: 16

### 5. Seaborn
**What it does**: Makes beautiful, easy-to-read statistical charts.  
**Example**:
{%- highlight python -%}
import seaborn as sns
import matplotlib.pyplot as plt
sns.barplot(x=['A', 'B', 'C'], y=[5, 10, 15])
plt.show()
#=> Output: (As shown in the image below) Displays a bar chart with values 5, 10, and 15 for categories A, B, and C
{%- endhighlight -%}

Output:
<figure>
	<img src="{{site.url}}/{{site.baseurl}}/testing-code/seaborn-eg.png" alt=""> 
	<figcaption>Output: Seaborn Example</figcaption>
</figure>

* **Usability**: 3.5/5
* **Beginner-friendliness**: 5/5
* **Versatility**: 4/5
* **[Ranking on GeeksforGeeks](https://www.geeksforgeeks.org/python-libraries-to-know/#9-seaborn)**: 9

## Conclusion
These five libraries are essential tools for any data science student. Whether you're just starting out or looking to expand your skills, mastering these libraries will give you a strong foundation in Python for data science. Remember, the key to learning is consistency and practice. Start small but start NOW!

