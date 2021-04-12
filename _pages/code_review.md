---
layout: page
title: Code Review
---

## Overview
---
Code review is an essential step in development that is put in place to verify the work being done. It can cover a multitude of topics from syntax, formatting, and naming conventions to proper structure usage, security, and efficiency. More personally, it is a fantastic way to grow as a developer. A code review will undoubtedly make the product much better but also plays an extremely important role in learning. It can occur at anytime and is usually best suited to occurring earlier in the pipeline and frequently. Waiting until the end of development usually means having to double back on work previously considered completed.

In my professional experience, I have participated in two distinct types of code review. One being focused just on the product, and the other on the product and the team. The former just wanted a working product that met the specifications and was up to standards. The latter did the same, of course, but also understood the concept of team building and personal growth. It is no surprise that the latter became an invaluable asset after working so long in places with the former. Encouraging one another to learn from each other and really pick their brain and get a sense of their own logic is a great way to get a look into developing from different perspectives. Much like having a proofreader or third-party review your asset you have been staring at for days or weeks, code reviews can grant a different perspective or fresh pair of eyes to determine a solution.



## Best/Uncommon Practices
---
Performant code tops my list of best practices for code reviews. This is particularly important when working with game engines and/or code that runs constantly. There are hundreds of ways to get an object reference to something in your scene, but if the solution entails getting references 60 or 90 (or more) times per second, it better be performance minded if having to search through large swaths of objects. Being mindful of expensive calls and implementations is a staple in the games industry and one that relies heavily on experience; experience that often comes by way of learning from code reviews.

Naming and commenting are my second big-ticket items for code reviews. If the original developer is the only one who can understand the code right away because of poor naming or lack of comments, there WILL be problems later. Ensuring descriptive yet concise variable and function naming means code or modules are that much simpler to understand quickly and easy to pick up for anyone coming in to modify existing code. Useful and descriptive comments will also allow for much quicker comprehension.

## Application Code Review
---
{% include youtubePlayer.html id="Lxgj_8yOUfQ" %}
