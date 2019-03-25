---
title: Sprint Blog Post 2
description: Sprint Blog Post 2
date: "2019-03-23T23:46:37.121Z"
---




<strong>Part 1 - Indvidual Accomplishments this Sprint:</strong><br>
This week was the integration part of our Labs Project. We started off the week divying up the API's to connect to the project. I chose the Zipcode api to connect to our create invoice form. Next I came up with a paragraph for our landing page describing our product and the 3 free credits you can get for siging up. I next researched some react testing library tests and enacted some for the landing page. Lastly I added snapshot testing and basic render testing to every component.

<strong>PR links:</strong><br>
https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/46

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/54

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/56

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/59

<strong>Trello board card names I worked on:</strong><br>
1. Landing page testing<br>
2. Marketing Area: Tell Users about free coins<br>
3. Snapshot testing
4. ZipCodeAPI.com (connect for auto-fill city & state)

<strong>Detailed Analysis:</strong><br>
For my detailed analysis I'm going to talk about my PR # 46.
In this ticket I connected the Zipcode Api to the create invoice form. We are using the Zipcode api to autofill the city and state on the form once a user enters a zipcode. First I had to sign up with the zipcode api website to get an api key. I next had to register our domain name to get a client key to use in the javascript function. After that I went to the create invoice form that my teamate created. It took me a good amount of time to study his code and figure out how he had things set up so I could integrate the api properly. The example function from the api docs used fetch and jquery so I had to take time to change it to plain javascript and axios. I ended up having to reach out to my pm because I was having trouble with state being one step behind the users input which was causing my api to never fire. In the end, by calling my Zipcode api function in the zipcode change handler function my teamate made, I was able to caputure the complete zipcode entered by the user and call the api and then autofill the city and state in the form.
<strong><br>Part 2 - Milestone Reflections:</strong><br>
The milestones for this sprint were to integrate all the components that make up the app, Including OAuth. To help the team solidify as a group I try to always give credit for all the accomplishments each individual team member has contributed to the project. To make sure that everyone on the team has a voice I make sure to ask each persons opinion on which apis they wanted and what to integrate first. As a group our biggest strength so far has been communication. We have daily standups and clearly go around the group led by our pm saying what we have been working on and what we will be working on. Our biggest obstacle this milestone was the google Oath suddenly not working right before the sprint check in with FJ. Earlier in the day the google OAuth was working locally on a teammates comput but stopped working on the domain. We all hopped in a zoom and started brain storming solutions and using Google-Fu. We weren't able to figure it out before check in but were able to show our other api integration such as my zipcode api and the google calendar api. We told FJ we were confident we would have it fixed by saturday. Not long after the check in. A teammate realized he had put a slash in the wrong way. After the slash was fixed the OAuth started working properly.




