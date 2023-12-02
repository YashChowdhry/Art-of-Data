---
layout: post
title: Lab 1 - Digimon
subtitle: Exploring the basics of the data analysis using csv
cover-img: /assets/img/download.jpg
thumbnail-img: /assets/img/download2.jpg
share-img: /assets/img/download3.jpg
tags: [books, test]
---

Question 1: the average speed of all Digimon was roughly 120.4

Lets breakdown the code to understand how we were able to access the dataset via the API:

To access the API, python requires us to use the **requests** library. This library is used to make HTTP requests which simplifies the process of retrieving HTML content from websites.

~~~
Import requests
~~~

How do we actually send over the request the website? 

~~~
payload = {"key": "YashArtOfDataKEY123ABCsecret", "idx": idx} 
	url = f"https://afeingoldhm.pythonanywhere.com/socks"
	response = requests.get(url, params = payload)
~~~

The **payload** contains two key-value pairs, the key and idx. The key was needed to access the API, it serves as a password, and the idx was used to retrieve the information of a given index, it was a line by line process.  The url variable stores the url of the API with the specific endpoint we are working with. We then use the function **requests.get()** to actually make the request to the indicated url, and it provides the payload, the parameters needed to access the API. 


Question 2: sample: (“Memory”, “10”) returns 5

Question 3: a team is ['Koromon', 'Tsunomon', 'Tsumemon']

Question 4: This lab was easily translatable from the penguins practice, so I relied mainly on that. The syntax was more of a struggle than the problem solving aspect of the lab. Each problem has a simple approach except for question three. I had begun to write a code that would effectively tell me each possible sequence of teams that would satisfy the criteria because I didn’t want to find an easy way out, but was unable to do so. As we were walking home, I asked Thomas his approach which was the one I had already thought of, searching for each Digimon with a memory less than 5 and attack greater than 100. I use this approach in my code but am still trying to figure out a way to find every possible combination. 
~~~
if int(row["Memory"]) <= 5 and int(row["Atk"]) >= 100:
~~~
Another struggle I encountered was the way in which my files are stored. I still have yet to move around my files, but Feingold was able to figure out where I went wrong.
~~~
with open("digimon - digimon.csv", "r") as f:
~~~

Originally, I had thought that writing this type of code was very difficult, but the moment I took some time to really understand what each line of code did, I truly understood how the code was running and now it is a lot easier and frankly more fun.
