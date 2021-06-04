---
title: Paciolan - SDM WebApp Project
category: Development
category_slug: f-design f-dev
type: content
image: assets/img/Paciolan/pac.jpg

---
 
**INTRODUCTION**<br>
 
The project is a web-based application that involves UX design and implementation of the design. We are tasked with the job of redesigning a previous model and adding additional features and functionalities. This application uses messaging architecture to manage metadata for events such as enabling near-field communication (NFC), event relations, etc. This project utilizes tools like React, JavaScript, NodeJS, Express, and Kafka. In this project, we will mostly focus on the Front End web application and managing metadata from events of the application. This project will be catering to customers/clients like the Pac8 collegiate teams and others that utilize the main tool. The tool we are developing will mostly focus on allowing our clients to modify or enable a few features for their events, and to display metadata.<br><br>

**TEAM** <br>
><br>**Thu Huynh, Phuoc Trinh, Sazeda Sultana, Gordon Chan, Lucy Cao**<br><br>

|    My Roles    | Duration |    Tool     |
| :------------: | :------: | :---------: |
| Front-end Developer | 6 months  |    React.js    |


<br>

**TARGET AUDIENCES**
- Directors of ticket operations<br>

**GOALS**<br>
- Allow users to conduct freeform search
- Allow users to make a bulk update to multiple events
- Allow users to save changes to the metadata database<br> 

**ASSUMPTIONS**<br>
- Users of the application will already have all the necessary information to access the tool.
- The majority of our users will be accessing the web-app via devices with a screen size over 900 pixels.
- Control flow cross platforms will have the same logical flow.<br>

**PERSONA & SCENARIO**<br>
<img src="/assets/img/Paciolan/Picture1.png" height="500"/> <br>
Figure 1.1. Persona 1 - Robert.
<br>

Scenario: 
Robert, as the director of ticket operations,  wants to change the settings of his events so that they run smoothly.
He wants to enable NFC for all of his events in the spring 2020 season, so he goes to the search page and searches “spring 2020”. His results are displayed and he selects all after hitting the update button. He then checks the NFC checkboxes so that they are enabled. He confirms his changes and sees the summary page. 


**FUNCTIONAL REQUIREMENTS**<br> <br>

<img src="/assets/img/Paciolan/useCase.png" height="600"/> <br>
Figure 1.1. Use-Case Diagram for SDM Web App’s Corporate Site.

**USE CASE 1**   Conduct freeform search in the SDM<br>
Priority: MUST HAVE

Basic Flow
1.	The user logs in to the SDM system.
2.	The user types keywords into the search box.
3.	The user hits enter.
4.	The results matching the keywords will be displayed in the search result page. 



**USE CASE 2**   Make a bulk update<br>
Priority: MUST HAVE

Basic Flow
1.	The user logs in to the SDM system.
2.	The user types keywords into the search box.
3.	The user hits enter.
4.	The results matching the keywords will be displayed. 
5.	The user presses the update button.
6.	Checkboxes will appear next to results.
7.	The user checks events they want to update.
8.	The user selects the fields of the events they want to update.
9.	The user hits confirm.
10.	The user is presented with a confirmation (summary) page.



**USE CASE 3**   Save changes to the metadata database<br>
Priority: MUST HAVE

Basic Flow
1.	The user hits confirm to confirm their changes.
2.	Once the user makes changes to the event(s), the current metadata of those will be retrieved from MTD
3.	The system compares the old data with the new ones and makes an update.
4.	The metadata then will be saved to Cassandra.


**USE CASE 4**  Users should be able to enable integration for each of the events, (SMS, check-in, NFC)<br>
Priority: MUST HAVE

Basic Flow
1.	The user enters their search
2.	Search results come up with the events related
3.	Application displays enabled integration for SMS, check-in, NFC on each event
4.	Users select a single event
5.	User choose to enable or disable their preferred settings on the detail page (which already exists)


<br>
**Software DESIGN**<br><br>
I was assigned to work on the front-end for the Search page, the Bulk Update page and the filtering function for the Search Result page using React.js with Webpack. <br><br>
Unfortunately, this is an internal web application, so it isn't public outside of Paciolan and their partners. I've include some of the mock-ups which I then implemented below.<br><br>
**Search Page**<br> 
In the old design, the search function was conducted only using the event code and season code. Following below is the new design that aims to convert it into a freeform search where the user can enter any keyword relevant to the event into the search box, and the system will return them a list of matching events. <br><br>

<img src="/assets/img/Paciolan/search.png"/> <br><br>

**Search Result Page** 
The 3 key functions that the search result page has to accomplish are to lead the user to an individual item detail page, to give a brief visualize of the state of each item, and to lead the user to the bulk update page. <br>
Notable features: 
- Filter events based on NFC/SMS/Barcode Sharing status
- Sort events based on date/name <br><br>
<img src="/assets/img/Paciolan/filter.png" height="600"/> <br><br>

**Bulk Update**<br><br>
The page displays a list of events taken from the search result page for users to choose from to be bulk updated. It shows different bulk update options and to enable or disable SMS, NFC. <br>
Notable features: 
- Update multiple events at once
- Provide errors prevention mechanisms
- Calling API endpoint to save the changes to the database
- Sort events based on date/name <br><br>
<img src="/assets/img/Paciolan/bulk.png" height="700"/> <br><br>

