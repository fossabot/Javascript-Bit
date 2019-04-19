---
title: Commonly asked javascript interview questions
subTitle: Frontend and UI interview questions
category: "interview"
cover: photo-1490474418585-ba9bad8fd0ea-cover.jpg
---

I'm posting a few questions that I have come across in some of the interviews I gave. I'll probably sort it company-wise in my later posts. To save time, I have skipped the answers to some questions; they are easy enough to find on Google. I've also mentioned the chances of any developer coming across these questions in an interview.

---

**What is the difference between `GET` and `POST` requests? (High)**
**How will you optimize the loading of a page? What are the good practices that you can follow? (Medium)**

- Load the Javascript at the bottom of the page. Javascript is content that is not visible and should be loaded last.
- Optimize image size. Use compressed formats for images.
- Reduce the number of HTML tags.
- Cache the page but try finding an optimum trade-off for the new loading of a page.
- Minify .js and .css files.
- Use templating engines.
- Use Ajax to load non-essential content

**How will you fix Javascript code that tends to make old web browsers unresponsive? What will you do? (Low)**

Optimize the javascript and ensure that it does not contain functions that are re-run all the time. Remove event handlers like resize() and other event handlers that may be buggy or causing memory leaks.

**What other performance changes can you make to your Javascript if you are using plugins like jQuery? (Medium - must know)**

Avoid using jQuery whenever possible. For simple tasks like fetching elements, jQuery causes bloating since it uses the Façade design pattern. Façade pattern provides high abstraction and hence, in some cases tends to bring the performance down.
e.g. avoid $(this).val(). Instead, use this.value
Using document.getElementById() is known to be much faster than $(‘#someId’).get(0).

**How will you use theming on a web application? Suppose you want to have multiple themes on the web page. How will you achieve it? (Low)**

There are a few ways to do this. If your web application is enormous, then you should use AMD(Asynchronous Module Definition)/require.js to switch the CSS styles while removing the old ones. If it is small enough, then you can use pure Javascript and CSS hierarchy to achieve the design. 

**You are a poor shopkeeper who can afford only four weights. However, you have to able to weigh every weight between 1kg and 40kg. How will you achieve this? (Puzzle)**

**How will you detect a cycle in a linked list? You can't store a flag into the Nodes of the linked list. Storing the nodes results in memory overflow in case the linked list has a large number of nodes. (High)**

[GeekForGeeks](https://www.geeksforgeeks.org/detect-and-remove-loop-in-a-linked-list/)

**Write a function that matches these strings and returns the necessary solution. (Low)**

Str1 = ‘abc’ | str2 = ‘abbcc’ -> True
Str1 = ‘ab’ | str2 = ‘aaabb’ -> True
Str1 = ‘ace’ | str2 = ‘aee’ -> False
Str1 = ‘abcd’ | str2 = ‘dcab’ -> True

**Define a function log() that can take up any number of arguments, appends ‘app’ and prints all the parameters separated by a space. (Low)**

**What is the arguments array? (High)**
