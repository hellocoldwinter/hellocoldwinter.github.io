---
title: Selector - Choice Making Assistance
category: UI/UX Design
category_slug: f-design
type: content
image: assets/img/Selector/thumbnail.png
button_url: project/index.html
---

<br>

**CONTEXT** <br>
Sometimes it is difficult to come to a mutual agreement regarding what to do together. This decision is even harder to make if it is a big group of people. Some examples could be choosing which games on Steam to play together, which movies on Netflix to create a watch party for, or even what to do in general. Not only making the decision, coming up with a list of options in the first place can be a challenge as well.
<br>
The app will offer users a way to customize their list of options -whatever it is. It needs to be fun to use as well because the process of picking something over something else is already a heated discussion where most people want their choice to be picked. It will also need a recommendation feature for users who just want suggestions. 
<br><br>

**FUNCTIONALITY** <br>
* Help people make their choices among various options in different categories (restaurants, movies, games, traveling destinations…) using different methods - Swiping, Dice, Randomize
* Share list between users using links
* Provide recommendations/list of options for users if they don’t have any idea in mind (restaurants, movies, games, traveling destinations…)
<br><br>

**TARGET AUDIENCE** <br>
Anyone who wants to spend time with their friends/family and has a hard time deciding what to do among a list of options and/or anyone who needs suggestions regarding what to do and open to exploring new options.
<br><br>

**DESIGN CHOICE** <br><br>
<ins>Approach 1: Recommendations are randomly generated</ins>
> Customers are presented with different categories (movies, games, restaurants, events…)
Customers choose the category based on what they want to do with their friends/family. <br>
> The app will provide customers some basic filters to narrow down their list. <br>
> The app then proceeds to send a request to external APIs to get data based on the user’s filters then randomize and put them into a list. 
<br>
<ins>Rationale for approach 1:</ins> <br>
> The list is not completely random, rather, it takes the user’s preference/restrictions into consideration. This approach generally offers a great customization/personalization capability. <br>
> This approach saves customers’ time by not forcing them to actually come up with ideas. <br>
> This approach also opens a possibility that customers would have some new and interesting options that they may not think about. <br><br>

<ins>Approach 2: Recommendations are essentially other users’ lists</ins>
> There would be a ‘board’ tab in the app where recent lists of options created by other users are displayed. <br>
> Users can either search these available lists by typing keywords or browse them by category (depending on how the creator categorizes them) <br>
> After the user taps on a list, they can decide whether they want to use that list as their list or not. 
<br>
<ins>Rationale for approach 2:</ins> <br>
> The previously created list can be recycled in this approach. <br>
> There is more of a sense of community here as the user knows that their list is set up by another real user. <br>
> Real users can come up with many interesting ideas that otherwise would not be available using randomization algorithms. <br><br>

<ins>Approach 3: Recommendations are collected from other participants in the party</ins>
> There will be a link that the user can share with other participants in their party either by email, SMS or social media message. <br>
> Each of these participants can add items to the list. <br>
> After the participants are done with adding items, there will be a button for them to notify the original creator. The original creator then can finalize the list and start sharing the list 
<br>
<ins>Rationale for approach 3:</ins> <br>
> The recommendations in this approach will be more relevant as they are provided by the participants directly. <br>
> There will be less chance that there will be an option that everyone in the party dislikes. <br>
> There is more interaction between participants in this case. <br><br>

<ins>Final decision and design defense </ins> <br>
I would ultimately pick the first approach if I can only pick one because it meets the criteria regarding users’ preferences/restrictions. It can also satisfy the “explorer” type of users who like new ideas and trying new things. By leaving the job of coming up with list items to the randomization algorithms, it will save the user a lot of time, especially if compared to approach 2 and 3. In the second approach, even though the final list can be quite interesting, there are more chances that there would be items that are completely out of radar to the user (for diners, it may be restaurants that are too far, for gamers it may be first-person shooter games that gamers with motion sickness cannot play…) Also for approach 2, it would need a database to store all the users’ lists and the database will require regular maintenance. For approach 3, its weakness would be the amount of time it takes to get input from other participants. For a huge group of people, it will be very time-consuming.<br><br>

**QOC DIAGRAM** <br>
<img src="/assets/img/Selector/QOC.jpg" alt="qocdiagram" title="questionchoice"/><br><br>



