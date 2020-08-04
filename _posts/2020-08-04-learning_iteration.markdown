---
layout: post
title:      "Understanding Fetch"
date:       2020-08-04 12:32:22 -0400
permalink:  learning_iteration
---

It took me a while to wrap my head around the concept of the fetch method in javascript.

**Let's break it down**

The first step is calling the fetch method that takes any API URL which is pass in as a string.
```
fetch('http://example.com/movies.json')
```
Next step is the  ```.then()``` this is where things got a littlte confusing for me but essentially  
the  ```.then()``` is taking the data from which ever API URL you place in the   ```fetch()```and  passing the ```response ```
which means it is getting all of the infomation the API has and then we want to turn that into a``` json()``` format.

```
  .then(response => response.json())
```

Next the second ``` .then()``` is where the data that you are pulling from the URL is coming in and you can 
name it whatever you want ```data ```or whatever naming convention that helps you understand what is coming back if you pull movies from a movie API you would call it ```movies``` it doesn't matter. Then it is a good practice to console log this ```data``` to see what objects you're getting back that's where you ```console.log(data)``` and open up the inspector.

```
 .then(data => console.log(data));
 
```
and that's fetch the basic concept of fetch!

```
fetch('http://example.com/movies.json')
  .then(response => response.json())
  .then(data => console.log(data));
```


